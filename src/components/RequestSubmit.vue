<template>
  <div class="request">
    <div class="request_submit">
      <div class="request_submit-logo" >
        <img src="/img/logoblack.svg">
        </div>
       <div class="request_submit-description">
        <p>GET IN TOUCH!</p>
         <feedback-form id="request-form"/>
      </div>
    </div>
  </div>

</template>


<style scoped>
p{
  padding-top: 20px;
  padding-bottom: 20px;
}
.request {
  min-height: 100vh;
  text-transform: none;
  text-align: center;
  display: flex;
  background: #ffffff;
  width: 100%;
  color: black;
  justify-content: center;
  align-items: center;

}
.request_submit {
  padding-bottom: 30px;
  padding-top: 30px;
  height: 90%;
  width: 90%;
  display: flex;
  align-items: center;
}
@media screen and (max-width: 600px) {
  .request_submit {
    flex-flow: column;
  }
}

@media screen and (min-width: 600px) {
  p {
    text-align: start;
  }
}
.request_submit-logo {
  width: 50%;
}
.request_submit-logo img{
  width: 70%;
}

.request_submit-description {
  width: 50%;
}
</style>

<script>
import FeedbackForm from "components/FeedbackForm.vue";
import {ref} from 'vue'

export default {
  name: 'request-submit',
  components: {FeedbackForm},
  setup() {
    return {}
  }
}
</script>
