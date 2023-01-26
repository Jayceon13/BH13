<template>
  <div class="request">
    <div class="request_submit">
      <div class="video-request">
        <video class="background-request" autoplay muted loop playsinline poster="" >
          <source src="/video/vdo.mp4" type="video/mp4">
        </video>
      </div>
       <div class="request_submit-description">
         <feedback-form id="request-form"/>
      </div>
    </div>
  </div>

</template>


<style scoped>
.video-request{
  width: 50%;
  height: 100%;
  overflow: hidden;
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
  height: 600px;
  text-transform: none;
  text-align: center;
  display: flex;
  width: 100%;
  color: black;
  justify-content: center;
  align-items: center;

}
.request_submit {
  padding-bottom: 30px;
  padding-top: 30px;
  height: 600px;
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
  background: white;
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
    height: 100vh;
    margin-top: 200px;
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
