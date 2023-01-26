<template>
  <div class="request">
    <div class="request_submit">
      <div class="video-request">
        <q-parallax
          :height="600"
          :speed="2"
          class="parallax"
          src="/img/duck.webp"
        >
        </q-parallax>
      </div>
       <div class="request_submit-description">
         <feedback-form id="request-form"/>
      </div>
    </div>
  </div>

</template>


<style scoped>
.parallax{
  opacity: 0.3;
}
.video-request{
  width: 50%;
  height: 100%;
}
.background-request {
  background: black;
  opacity: 0.3;
  height: 100%;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  transform: scale(2);
}
p{
  padding-top: 20px;
  padding-bottom: 20px;
}
.request {
  height: auto;
  text-transform: none;
  text-align: center;
  display: flex;
  width: 100%;
  color: black;
  align-items: center;

}
.request_submit {
  padding-bottom: 30px;
  padding-top: 30px;
  height: auto;
  width: 100%;
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

.request_submit-description {
  width: 50%;

  height: 100%;
}
@media screen and (max-width: 600px) {
  .request_submit-description {
    width: 70%;
  }
  .video-request{
    width: 70%;
  }
  .request_submit {
    height: auto;
  }
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
