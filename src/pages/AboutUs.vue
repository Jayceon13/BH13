<template>
  <div class="about">
    <div class="about_info">
      <div class="about_info-main">
        <div class="about_info-main-name">
          <div class="main_page-home--logo"
               data-aos="zoom-in"
               data-aos-easing="ease"
               data-aos-delay="800">
            <img class="logo" src="/img/logo.png">
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


        <!--          <div class="about_info-main-description-mobile">-->


        <!--            <h3 class="about-h3" data-aos="zoom-in"-->
        <!--            >OUR VALUES</h3>-->
        <!--            <p class="about-border-description"-->
        <!--               data-aos="fade-up-right"-->
        <!--            >TRANSPARENCY - Our priority is integrity and honesty in all our endeavours. Thus, we have carefully-->
        <!--              constructed a system of weekly reports ensuring the client remains aware of all the on-goings.</p>-->
        <!--            <p class="about-border-description"-->
        <!--               data-aos="fade-up-left"-->
        <!--            >FLEXIBILITY - We will go above and beyond to make sure the client’s expectations are met. Time is of the-->
        <!--              essence for everyone and that is why we keep flexibility as one of our strengths.</p>-->
        <!--            <p class="about-border-description"-->
        <!--               data-aos="fade-up-right"-->
        <!--            >CREATIVITY - When it comes to creative solutions, E&A professionals never take the easy route. Our-->
        <!--              intention is to make your brand stand out from the rest. Engaging the crowd in the digital sphere is what-->
        <!--              we are best at.</p>-->
        <!--            <p class="about-border-description"-->
        <!--               data-aos="fade-up-left"-->
        <!--            >PERCEPTION - Understanding the brand we are working with, is a top priority at E&A. No matter the industry,-->
        <!--              we put a massive amount of emphasis into seeing who we are working with and what are the values of the-->
        <!--              client.</p>-->

        <!--          </div>-->

        <div class="about_info-main-description">


          <h2 class="about-h2" data-aos="zoom-in"
          >OUR VALUES</h2>


          <div class="about_desktop">

            <div class="about_desktop-description about-border-description"
                 data-aos="fade-up-right">

              <div class="about_desktop-description-name">
                <h3 class="desktop-description-h3">TRANSPARENCY - </h3>
              </div>
              <div class="about_desktop-description-info">
                <p class=" desktop-description-p"

                >Our priority is integrity and honesty in all our endeavours. Thus,<sup/> we have carefully constructed a system
                  of weekly reports ensuring the client remains aware of all the on-goings.</p>

              </div>

            </div>

            <div class="about_desktop-description about-border-description"
                 data-aos="fade-up-left">

              <div class="about_desktop-description-name">
                <h3 class="desktop-description-h3">FLEXIBILITY - </h3>
              </div>
              <div class="about_description-desktop-info">
                <p class="desktop-description-p"
                >We will go above and beyond to make sure the client’s expectations are met. Time is of the essence for
                  everyone and that is why we keep flexibility as one of our strengths.</p>
              </div>

            </div>




            <div class="about_desktop-description about-border-description"
                 data-aos="fade-up-right">

              <div class="about_desktop-description-name">
                <h3 class="desktop-description-h3">CREATIVITY - </h3>
              </div>
              <div class="about_description-desktop-info">
                <p class="desktop-description-p"

                >When it comes to creative solutions,<sup/> E&A professionals never take the easy route. Our intention is to
                  make your brand stand out from the rest. Engaging the crowd in the digital sphere is what we are best
                  at.</p>
              </div>

            </div>




            <div class="about_desktop-description about-border-description"
                 data-aos="fade-up-left">

              <div class="about_desktop-description-name">
                <h3 class="desktop-description-h3">PERCEPTION - </h3>
              </div>
              <div class="about_desktop-description-info">
                <p class="desktop-description-p"

                >Understanding the brand we are working with, is a top priority at E&A. No matter the industry, we put a
                  massive amount of emphasis into seeing who we are working with and what are the values of the
                  client.</p>
              </div>

            </div>









          </div>
        </div>
      </div>
    </div>
    <request-submit id="request-form"/>
  </div>
</template>

<script>
import RequestSubmit from "components/RequestSubmit";

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
.about-h1 {
  font-size: 34px;
  font-weight: bold;
  letter-spacing: 2px;
  line-height: normal;

}
@media screen and (max-width: 900px) {
  .about-h1 {
    font-size: 26px;
  }
}
@media screen and (max-width: 650px) {
  .about-h1 {
    font-size: 22px;
    margin: 20px 0;
  }
}
@media screen and (max-width: 450px) {
  .about-h1 {
    letter-spacing: 0;
    font-size: 18px;

  }
}

.about-h2 {
  font-size: 28px;
  letter-spacing: 2px;
  line-height: normal;
}
@media screen and (max-width: 900px) {
  .about-h2 {
    font-size: 24px;
  }
}
@media screen and (max-width: 650px) {
  .about-h2 {
    font-size: 18px;
  }
}
@media screen and (max-width: 450px) {
  .about-h2 {
    letter-spacing: 0;
    font-size: 16px;
  }
}
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
  width: 100%;
  text-align: center;
}

.about_info {
  width: 80%;
}

.about_info-main{
  text-align: -webkit-center;
}

.about_info-main-description{
  width: 80%;
}

.about_info-main-name {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

}

/*.about_info-main-description-mobile {*/
/*  height: 0;*/
/*  display: flex;*/
/*  flex-direction: column;*/
/*  align-items: center;*/
/*  opacity: 0;*/
/*}*/

/*@media screen and (max-width: 650px) {*/
/*  .about_info-main-description-mobile {*/
/*    height: 100%;*/
/*    opacity: 1;*/
/*  }*/
/*}*/

.about_desktop {
  display: flex;
  flex-direction: column;
  width: 100%;
  text-align: left;
  border-left: solid;
  border-color: white;
  border-width: 3px;
  margin: 30px 0;
}
@media screen and (max-width: 650px) {
  .about_desktop {
    border: none;
  }
}

.about_desktop-description {
  display: flex;
}
@media screen and (max-width: 800px) {
  .about_desktop-description {
    display: flex;
    flex-direction: column;
    margin: 20px 0 20px;
  }
}
@media screen and (min-width: 650px) {
  .about_desktop-description {

    margin: 20px 0 20px 30px;
  }
}

.about_desktop-description-name {
  display: flex;
  align-items: center;
  min-width: 30%;

}
@media screen and (max-width: 650px) {
  .about_desktop-description-name {
    display: flex;
    align-items: center;
    width: 100%;

  }
}
.about_desktop-description-info{
  width: 70%;
}

@media screen and (max-width: 800px) {
  .about_desktop-description-info{
    width: 100%;
  }
}

.desktop-description-h3 {
  font-size: 20px;
  margin: 0;
}
.desktop-description-p {
  font-size: 16px;
  margin: 0;
  font-weight: 200;
}

/*@media screen and (max-width: 650px) {*/
/*  .about_info-main-description-mobile {*/
/*    height: 100%;*/
/*    opacity: 1;*/
/*  }*/
/*}*/

/*.about_info-main-description {*/
/*  height: 0;*/
/*  display: flex;*/
/*  flex-direction: column;*/
/*  opacity: 0;*/
/*}*/

/*@media screen and (min-width: 650px) {*/
/*  .about_info-main-description {*/
/*    height: 100%;*/
/*    opacity: 1;*/
/*  }*/
/*}*/

@media screen and (max-width: 650px) {
  .about-border-description {
    padding: 20px;
    border-width: 2px;
    border-radius: 20px;
    background-position: center center;
    border-color: #ffffff;
    border-style: solid;
  }
}

@media screen and (max-width: 650px) {
  .desktop-description-h3 {
    font-size: 16px;
    margin: 0;
  }
}
@media screen and (max-width: 1000px) {
  .desktop-description-h3 {
    font-size: 16px;
  }
}
@media screen and (max-width: 650px) {
  .desktop-description-p {
    font-size: 16px;
    margin: 0;
  }
}



</style>

