<template>
  <q-form
    @submit="onSubmit"
    @reset="onReset"
    class="form"
    method="post"
  >
    <q-input
      class="input"
      filled
      v-model="namesur"
      label="Your name *"
      lazy-rules
      :rules="[ val => val && val.length > 2 || 'Please type something']"
    />

    <q-input
      class="input"
      filled
      v-model="phone"
      label="Phone number *"
      lazy-rules
      :rules="[
        val => val && val.length > 6 || 'Please type your phone number',
      ]"
    />
    <q-input
      class="input"
      filled
      v-model="email"
      label="E-mail *"
      :rules="[
       (val, rules) => rules.email(val) || 'Please enter a valid email address'
       ]"
    />

    <q-input
      class="input"
      filled
      v-model="request"
      label="Your request *"
      type="textarea"
      lazy-rules
      :rules="[
        val => val && val.length > 2 || 'Please type your request',
      ]"
    />

    <div>
      <q-btn label="Submit" type="submit" color="rebeccapurple" id="feedback-form" formaction="/.netlify/functions/send-email"/>
      <q-btn label="Reset" type="reset" color="white" flat class="q-ml-sm" />
    </div>
  </q-form>
  <alert-form :show="showAlert"></alert-form>
</template>

<style>
.form{
  padding: 30px;
  height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.q-field__inner{
  background: #9A01D0;
}

.q-field__label{
  color: white;
}

</style>

<script>
import AlertForm from "components/AlertForm.vue";
import axios from 'axios';
import { ref } from "vue"

export default {
  name: 'feedback-form',
  components: {AlertForm},

  setup() {
    const namesur = ref(null)
    const phone = ref(null)
    const email = ref(null)
    const request = ref(null)
    const showAlert = ref(false)

    // Метод, который меняет значение переменной showAlert
    const showAlertSuccess = () => {
      showAlert.value = !showAlert.value;
    };
    return {
      showAlert,
      showAlertSuccess,
      namesur,
      phone,
      email,
      request,
      async onSubmit() {
        try {
          const response = await axios.post('/.netlify/functions/send-email', {
            namesur: namesur.value,
            phone: phone.value,
            email: email.value,
            request: request.value
          });
          console.log(response.data);
          namesur.value = null
          phone.value = null
          email.value = null
          request.value = null
          showAlertSuccess()
          // Отображаем сообщение об успешной отправке формы
        } catch (error) {
          console.error(error);
        }
      },
      onReset() {
        namesur.value = null
        phone.value = null
        email.value = null
        request.value = null
      }
    };
  }
}
</script>

