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
          <div class="developers">
            <div class="developer-1">
              <q-avatar size="150px">
                <img src="/img/developer1.png">
              </q-avatar>
              <p>Hello everyone!</p>
            </div>
            <div class="developer-2">
              <q-avatar size="150px">
                <img src="/img/developer2.png">
              </q-avatar>
            </div>
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

.developers{
  display: flex;
  width: 100%;
  height: 400px;
}
.developer-1{
  width: 50%;
  text-align: center;
}
.developer-1 p{
  color: white;
}
.developer-2{
  width: 50%;
  text-align: center;
}



</style>

