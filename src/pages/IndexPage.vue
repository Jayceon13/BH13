<template>
  <q-page class="flex flex-center main">
    <video autoplay muted loop playsinline poster="" id="myVideo">
      <source src="" type="video/mp4">
    </video>
    <div class="main_page">
      <div class="main_page-home">
        <div class="main_page-home-left">
          <div class="main_page-home--name">
          </div>
          <div class="main_page-home--logo"
               data-aos="zoom-in"
               data-aos-easing="ease"
               data-aos-delay="800">
            <div class="overflow-hidden">
              <q-resize-observer @resize="onResize" :debounce="0" />

              <q-splitter
                id="photos"
                v-model="splitterModel"
                separator-class="bg-orange"
                separator-style="width: 3px"
                :limits="[0, 100]"
                :style="splitterStyle"
                before-class="overflow-hidden"
                after-class="overflow-hidden"
              >

                <template v-slot:before>
                  <img
                    src="/img/logo2.svg"
                    :width="width"
                    class="absolute-top-left"
                  />
                </template>

                <template v-slot:after>
                  <img
                    src="/img/logo1.svg"
                    :width="width"
                    class="absolute-top-right"
                  />
                </template>

              </q-splitter>
            </div>
          </div>
          <div class="main_page-home--name-right">

          </div>
        </div>
      </div>
      <div class="main_page-info">


        <div class="content">
          <div class="content-services"
               data-aos="zoom-in">
            <h2 class="main-h2">Services</h2>
          </div>
          <div class="cards-services">
            <div class="img-box">
            </div>
            <div class="card-1">
              <img src="/img/01.svg">
              <video class="video-1" autoplay muted loop playsinline poster="" id="myVideo">
                <source src="/video/cardsbackground.mp4" type="video/mp4">
              </video>
            </div>
            <div class="card-2">
              <img src="/img/02.svg">
              <video class="video-2" autoplay muted loop playsinline poster="" id="myVideo">
                <source src="/video/cardsbackground.mp4" type="video/mp4">
              </video>
            </div>
            <div class="card-3">
              <img src="/img/03.svg">
              <video class="video-3" autoplay muted loop playsinline poster="" id="myVideo">
                <source src="/video/cardsbackground.mp4" type="video/mp4">
              </video>
            </div>
          </div>


        </div>
      </div>
    </div>
    <request-submit id="request-form">
    </request-submit>
  </q-page>
</template>



<script>
import {defineComponent} from 'vue'
import RequestSubmit from "components/RequestSubmit.vue";
import { ref, computed } from 'vue'


export default defineComponent({
  name: 'IndexPage',
  components: {RequestSubmit},
  setup () {
    const width = ref(400)

    return {
      width,
      splitterModel: ref(50), // start at 50%

      splitterStyle: computed(() => ({
        height: Math.min(600, 0.66 * width.value) + 'px',
        width: width.value + 'px'
      })),

      onResize (info) {
        width.value = info.width
      }
    }
  }
  }
)
</script>

<style>

.overflow-hidden{
  height: 350px;
}
@media screen and (max-width: 1030px) {
  .overflow-hidden{
    height: 300px;
  }
}
@media screen and (max-width: 800px) {
  .overflow-hidden{
    height: 250px;
  }
}
@media screen and (max-width: 500px) {
  .overflow-hidden{
    height: 150px;
  }
}
.card-1{
  border-radius: 40px;
  margin: 25px;
  width: 335px;
  height: 480px;
  overflow: hidden;
}
.card-1 img{
  position: absolute;
  margin: 50px;
}
.card-2{
  border-radius: 40px;
  margin: 25px;
  width: 335px;
  height: 480px;
  overflow: hidden;
}
.card-2 img{
  position: absolute;
  margin-top: 50px;
  margin-left: 87px;
}
.card-3{
  border-radius: 40px;
  margin: 25px;
  width: 335px;
  height: 480px;
  overflow: hidden;
}
.card-3 img{
  position: absolute;
  margin-top: 50px;
  margin-left: 100px;
}
.video-1 {
  object-position: 0;
  opacity: 0.6;
  width: 335px;
  height: 480px;
  object-fit: cover;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  transform: scale(1.5);
}
.video-2 {
  object-position: -223px;
  opacity: 0.6;
  width: 335px;
  height: 480px;
  object-fit: cover;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  transform: scale(1.5);
}
.video-3 {
  object-position: -446px;
  opacity: 0.6;
  width: 335px;
  height: 480px;
  object-fit: cover;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: -1;
  transform: scale(1.5);
}

.cards-services{
  overflow: hidden;
  display: flex;
  margin-top: 100px;
}
@media screen and (max-width: 1120px) {
  .cards-services{
    flex-direction: column;
  }
}

.main-h1 {
  font-size: 34px;
  font-weight: bold;
  letter-spacing: 2px;
  line-height: normal;

}
@media screen and (max-width: 900px) {
  .main-h1 {
    font-size: 26px;
  }
}
@media screen and (max-width: 650px) {
  .main-h1 {
    font-size: 22px;
    margin: 20px 0;
  }
}
@media screen and (max-width: 450px) {
  .main-h1 {
    letter-spacing: 0;
    font-size: 18px;

  }
}

.main-h2 {
  font-size: 28px;
  letter-spacing: 2px;
  line-height: normal;
}
@media screen and (max-width: 900px) {
  .main-h2 {
    font-size: 24px;
  }
}
@media screen and (max-width: 650px) {
  .main-h2 {
    font-size: 18px;
  }
}
@media screen and (max-width: 450px) {
  .main-h2 {
    letter-spacing: 0;
    font-size: 16px;
  }
}

.main {
  text-transform: uppercase;
  color: white;
  font-size: 18px;
}

.main_page {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.main_page-info {
  display: flex;
  align-items: center;
  justify-content: center;
}


.main_page-home {
  width: 60%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
}

@media screen and (max-width: 450px) {
  .main_page-home {
    width: 80%;
    flex-flow: column;
    padding-right: 0px;
    justify-content: flex-start;
  }
}
.main_page-home-left {
  width: 100%;
}

.main_page-home--logo{
  text-align: center;
}

.main_page-home--name-right {
  margin-bottom: 40px;
  text-align: center;
}

.main_page-home--name {
  padding-left: 60px;
  display: flex;
  flex-direction: column;
}
@media screen and (max-width: 650px) {
  .main_page-home--name {
    padding-left: 0px;
  }
}
.logo {
  width: 500px
}
@media screen and (max-width: 1250px) {
  .logo {
    width: 400px
  }
}
@media screen and (max-width: 650px) {
  .logo {
    width: 300px
  }
}
@media screen and (max-width: 450px) {
  .logo {
    width: 300px
  }
}

.content {
  min-height: 100vh;
  width: 100%;
  padding-bottom: 60px;
}


.content_info {
  display: flex;
  flex-direction: column
}



.q-btn__content {
  display: flex;
  justify-content: space-between;

}

.btn-name {
  margin: 0px;
  font-size: 16px;
  text-align: center;
}
@media screen and (max-width: 450px) {
  .btn-name {
    font-size: 14px;
  }
}
.content-services {
  text-align: center;
}
.content_info-name {
  padding: 12px 8px;
}

.content_border-info {
  padding: 20px;
  border-width: 2px;
  border-radius: 20px;
  background-position: center center;
  border-color: #ffffff;
  border-style: solid;
}

@media screen and (min-width: 900px) {
  .content_border-info {
    margin: 20px 20px 20px 0px;
  }
}

.content_border-img {
  border-width: 2px;
  border-radius: 40px;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  border-color: #ffffff;
  border-style: solid;
}
@media screen and (min-width: 900px) {
  .content_border-img {
    margin: 20px 0px 20px 20px;
  }

}

.content_border-btn {
  margin: 20px 0px;
  border-width: 2px;
  border-radius: 20px;
  background-position: center center;
  border-color: #ffffff;
  border-style: solid;
}

.content_info-description {
  display: flex;
  align-items: center;
}

@media screen and (max-width: 450px) {
  .content_info-description {
    font-size: 12px;
  }
}
.content_info-description--info {
  width: 100%;
}
.content_info-description--img{
  max-height: 500px;
  max-width: 300px;
}

@media screen and (min-width: 900px) {
  .content_info-description--img {
    width: 50%;
    height: 100%
  }
}
@media screen and (max-width: 900px) {
  .content_info-description {
    flex-flow: column;
    margin: 0;
  }
}

@media screen and (max-width: 900px) {
  .content_info-description--info .content_border-info{
    width: 80%;
    text-align: center;
    margin: 0;
  }
}

@media screen and (max-width: 900px) {
  .content_info-description--img {
    margin-top: 20px;
    margin-bottom: 20px;
    width: 100%;
    text-align: center;
  }
}
.rotate-animation {
  rotate: 0;
  transition: 1s;
}

.rotate-animation-obj {
  transform: rotate(180deg);
  transition: 1s;
}

</style>
