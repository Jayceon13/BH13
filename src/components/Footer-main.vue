<template>
  <div class="footer">
  <div class="footer_info">
    <div class="footer-logo">
    <img class="footer_info-logo" src="/img/logoFooter.png">
    <div class="lecense" style="color: white">
      <p>© 2022 by E And A Group FZE<br>
        Dubai, United Arab Emirates</p>
    </div>
    </div>
    <div class="footer_btn">
      <div class="footer_info-btn-network">
        <a href="https://instagram.com/ea.mediagroup">
          <img class="btn-network btn-network-inst" src="/icons/instagram.svg">
        </a>
        <a href="https://wa.me/+971585996202">
          <img class="btn-network btn-network-wa" src="/icons/whatsapp.svg">
        </a>
      </div>

      <a class="btn-mail" href="mailto: inquiry@eamedia.ae">inquiry@eamedia.ae</a>
    </div>
  </div>
  </div>
</template>

<script>
import {ref} from 'vue'

export default {
  name: 'footer-main',
  setup() {
    return {}
  }
}
</script>

<style>
.footer {
  width: 100%;
  display: flex;
  justify-content: center;
  min-height: 200px;
}
.footer_info {
  width: 60%;
  text-transform: uppercase;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media screen and (max-width: 600px) {
  .footer_btn {
    width: 100%;
  }
}

@media screen and (max-width: 600px) {
  .footer-logo {
    width: 100%;
  }
}

@media screen and (max-width: 600px) {
  .footer_info {
    text-align: center;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin: 20px 0;
    flex-direction: column-reverse;
  }
}


.footer_info-btn-network {
  margin: 0 0 20px;
}
.footer_info-logo {
  width: 80px;
  margin-bottom: 20px;
  margin-top: 30px;
}
@media screen and (max-width: 450px) {
  .footer_info-logo {
    width: 60px;
  }
}

.btn-mail {
  text-decoration: none;
  color: white;
  font-size: 16px;
}
@media screen and (max-width: 450px) {
  .btn-mail {
    font-size: 12px;
  }
}

.btn-network {
  width: 30px;
  height: 30px;

}
.btn-network-inst{
  margin: 0 4px 0 0;
}
.btn-network-wa {
  margin: 0 0 0 4px;
}
</style>
