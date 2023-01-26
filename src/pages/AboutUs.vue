<template>
  <div class="about">
    <div class="about_info">
      <div class="about_info-main">
        <div class="about_info-main-name">
          <div class="main_page-home--logo"
               data-aos="zoom-in"
               data-aos-easing="ease"
               data-aos-delay="800">
            <img class="logo" src="/img/logo2.svg">
          </div>
          <div class="main_page-home--name-right">
            <h1 class="logo-name about-h1"
                data-aos="zoom-in"
                data-aos-easing="ease"
                data-aos-delay="1000">
              DIGITAL MARKETING AGENCY</h1>
            <h2 class="logo-name about-h2"
                data-aos="zoom-in"
                data-aos-easing="ease"
                data-aos-delay="1200">
              INNOVATE YOUR BUSINESS</h2>
          </div>
        </div>
      </div>
    </div>
    <request-submit id="request-form"/>
  </div>
</template>

<script>
import RequestSubmit from "components/RequestSubmit.vue";

export default {
  components: {RequestSubmit}
}
</script>


<style>



</style>

