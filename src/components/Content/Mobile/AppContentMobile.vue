<template>
  <div id="IDDevices" class="mobile">
    <div class="wrapper">
      <div class="mobile__photo-left">
        <img
          src="../../../assets/mobile.jpg"
          class="mobile__photo"
          alt="mobile"
        />
      </div>
      <div class="mobile__text-right">
        <div class="mobile__text-title">Excellent for Mobile Devices.</div>
        <div class="mobile__text-smoll">
          Qisi enim ad minim veniam, quis nostrud exerci tation ullamcorper
          suscipit lobortis nisl ut aliquip ex ea commodo consequat.
          Investigationes demonstraverunt lectores legere me lius quod ii legunt
          saepius claritas. Eodem modo typi, qui nunc nobis videntur parum
          clari, fiant sollemnes in futurum.
        </div>
        <div class="mobile__text-list">
          <ul class="mobile-list">
            <li class="mobile__list-item">
              Nam liber tempor cum soluta nobis eleifend option;
            </li>
            <li class="mobile__list-item">
              Option congue nihil imperdiet doming id quod mazim placerat facer;
            </li>
            <li class="mobile__list-item">
              Eodem modo typi, qui nunc nobis videntur parum futurum;
            </li>
            <li class="mobile__list-item">
              Investigationes demonstraverunt lectores
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.mobile {
  min-height: 700px;
}

.mobile .wrapper {
  display: flex;
  min-height: 700px;
}

.mobile .mobile__photo {
  width: 100%;
  height: auto;
  align-self: flex-end;
}

.mobile .mobile__photo-left {
  min-height: 700px;
  display: flex;
}

@media screen and (max-width: 1050px) {
  .mobile .mobile__photo-left {
    display: none;
  }
}

.mobile__text-right {
  align-self: center;
  max-width: 670px;
}

.mobile__text-right .mobile__text-title {
  font-size: 30px;
  color: #555555;
  font-family: "Raleway Semibold", sans-serif;
}

.mobile__text-right .mobile__text-smoll {
  font-size: 16px;
  color: #8c8c8c;
  padding: 30px 0 40px 30px;
}

.mobile__text-right .mobile-list {
  margin-left: 50px;
}

.mobile__text-right .mobile__list-item {
  background: url(../../../assets/mobile-arrow.png) no-repeat;
  padding: 1px 0 1px 50px;
  margin: 10px 0;
}
</style>
