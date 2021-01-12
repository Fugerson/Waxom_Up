<template>
  <div class="footer-bottom">
    <div class="wrapper">
      <div class="footer-bottom-box">
        <div class="footer-bottom-left">
          <div class="footer-bottom__left-text">
            Copyright © 2015<a href="#"> Waxom </a> Privacy Policy
            <a href="#">FAQ</a> Support
          </div>
        </div>
        <div class="footer-bottom-right">
          <div class="footer-bottom__right-text">
            Designed by <span>ThemeFire</span> Only on <span></span>Envato
            Market
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppFooterBottom"
};
</script>

<style scoped>
.footer-bottom {
  background-color: #111111;
  min-height: 110px;
}

.footer-bottom .footer-bottom-box {
  min-height: 110px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.footer-bottom .footer-bottom__left-text {
  color: #555555;
  font-size: 13px;
}

.footer-bottom .footer-bottom__right-text {
  color: #555555;
  font-size: 13px;
}

.footer-bottom .footer-bottom__left-text a:first-child {
  color: #959595;
  padding-right: 10px;
  border-right: 1px solid #232323;
}

.footer-bottom .footer-bottom__left-text a:last-child {
  cursor: pointer;
  color: #c7b299;
  padding: 0 10px;
  border-right: 1px solid #232323;
  border-left: 1px solid #232323;
}

.footer-bottom .footer-bottom__right-text span {
  color: #959595;
  padding-right: 10px;
  border-right: 1px solid #232323;
}
</style>
