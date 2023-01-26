<template>
  <q-layout view="hHh lpR fFf" style="font-weight: bold">

    <q-header elevated class="bg-primary" style="mix-blend-mode: difference">
      <q-toolbar show-if-above: false>
        <div class="header-components">
          <q-toolbar-title>
          </q-toolbar-title>

          <q-btn flat class=" header-btn"
                 @click="$router.push('/')">
            <img src="/img/logo2.svg">
          </q-btn>
          <div class="header-btn-right">
            <a class="header-btn-network" href="https://wa.me/+971585996202">
              <img class="header-btn-network-wa" src="/icons/whatsapp.svg">
            </a>
            <div :class="!rightDrawerOpen? 'hamburger hamburger--elastic': 'hamburger is-active hamburger--elastic'">
              <div class="hamburger-box" @click="toggleRightDrawer">
                <div class="hamburger-inner"></div>
              </div>
            </div>
          </div>
        </div>
      </q-toolbar>
    </q-header>
    <q-drawer
      v-model="rightDrawerOpen"
      behavior="mobile"
      :width="300"
      :breakpoint="400"
      side="right" bordered>
      <div class="menu">
        <div class="menu_burger">
          <img class="logo_burger" src="/img/logo2.svg">
          <div :class="!rightDrawerOpen? 'hamburger hamburger--elastic': 'hamburger is-active hamburger--elastic'" style="padding-right: 32px">
            <div class="hamburger-box" @click="toggleRightDrawer">
              <div class="hamburger-inner"></div>
            </div>
          </div>
        </div>
        <q-btn class="menu_burger-button" @click="$router.push('/')">Main</q-btn>
        <q-btn class="menu_burger-button" @click="$router.push('/about')">About us</q-btn>
      </div>
    </q-drawer>

    <q-btn @click="$router"></q-btn>

    <q-page-container style="padding-top: 40px">
      <router-view/>
      <footer-main id="contacts"/>
    </q-page-container>

  </q-layout>
</template>


<style>
@media screen and (max-width: 600px) {
  #contacts{
    margin-top: 200px;
  }
}

.menu {
  display: flex;
  flex-direction: column;
  color: black;
}

.menu_burger{
  display: flex;
  justify-content: space-between;
}
.menu_burger-button {
  padding: 10px 30px;
  font-size: 20px;
}

.q-btn:before {
  box-shadow: none;
}
.logo_burger {
  width: 80px;
  margin: 20px 30px;
}

.hamburger {
  display: flex;
  align-items: center;
  cursor: pointer;
  transition-property: opacity, filter;
  transition-duration: 0.15s;
  transition-timing-function: linear;
  font: inherit;
  color: inherit;
  text-transform: none;
  background-color: transparent;
  border: 0;
  overflow: visible;
  margin: 0 0 0 30px;

}

.hamburger:hover {
  opacity: 0.7;
}

.hamburger.is-active:hover {
  opacity: 0.7;
}

.hamburger.is-active .hamburger-inner,
.hamburger.is-active .hamburger-inner::before,
.hamburger.is-active .hamburger-inner::after {
  background-color: black;
}

.hamburger-box {
  width: 40px;
  height: 24px;
  display: inline-block;
  position: relative;
}

.hamburger-inner {
  display: block;
  top: 50%;
  margin-top: -2px;
}

.hamburger-inner, .hamburger-inner::before, .hamburger-inner::after {
  width: 40px;
  height: 4px;
  background-color: #ffffff;
  border-radius: 4px;
  position: absolute;
  transition-property: transform;
  transition-duration: 0.15s;
  transition-timing-function: ease;
}

.hamburger-inner::before, .hamburger-inner::after {
  content: "";
  display: block;
}

.hamburger-inner::before {
  top: -10px;
}

.hamburger-inner::after {
  bottom: -10px;
}

.hamburger--elastic .hamburger-inner {
  top: 2px;
  transition-duration: 0.275s;
  transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.hamburger--elastic .hamburger-inner::before {
  top: 10px;
  transition: opacity 0.125s 0.275s ease;
}

.hamburger--elastic .hamburger-inner::after {
  top: 20px;
  transition: transform 0.275s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.hamburger--elastic.is-active .hamburger-inner {
  transform: translate3d(0, 10px, 0) rotate(135deg);
  transition-delay: 0.075s;
}

.hamburger--elastic.is-active .hamburger-inner::before {
  transition-delay: 0s;
  opacity: 0;
}

.hamburger--elastic.is-active .hamburger-inner::after {
  transform: translate3d(0, -20px, 0) rotate(-270deg);
  transition-delay: 0.075s;
}


.logo-header {
  width: 100px;
}

.header-btn {
  display: flex;
  justify-content: space-between;
  font-weight: bold;
}
.header-btn img{
  width: 150px;
  background: none;
}

@media screen and (max-width: 450px) {
  .header-btn {
  }
}

.header-btn-right {
  display: flex;
  align-items: center;

}

.header-btn-network {
  width: 34px;
  height: 34px;
}
.header-btn-network-wa {
  width: 100%;
  height: 100%;
}
.header-logo-btn {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header_border-btn {
  border-width: 2px;
  border-radius: 30px;
  background-position: center center;
  border-color: #ffffff;
  border-style: solid;
}

.header-components {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
}
.menu_burger-button {
  font-weight: bold;
}

.q-toolbar__title {
  display: none;
}

.q-layout__shadow:after {
  box-shadow: none;
}
.q-btn {
  font-weight: bold;
}
.q-field__label {
  font-weight: bold;
}
</style>

<script>
import {ref} from 'vue'
import footerMain from "../components/Footer-main.vue";

export default {
  components: {
    footerMain
  },
  methods: {
    scrollToRequest() {
      document.getElementById('request-form').scrollIntoView({behavior: 'smooth'});
    },
  },
  setup() {
    const rightDrawerOpen = ref(false)
    const closeRightDrawer = () => {
      rightDrawerOpen.value = false
    }
    return {
      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value
      },
      closeRightDrawer
    }
  }
}

</script>

