<template>
  <div class="slider">
    <div class="wrapper">
      <div class="slider__box">
        <transition name="titleOne" appear>
          <h2 class="slider-title">Unique and Modern Design</h2>
        </transition>
        <transition name="titleTwo" appear>
          <h1 class="slider-bold">Portfolio PSD Template</h1>
        </transition>
        <transition name="titleThree" appear>
          <p class="slider-text">
            Nam liber tempor cum soluta nobis eleifend option congue nihil
            imperdiet doming id quod mazim placerat facer possim assum.
          </p>
        </transition>
        <transition name="Button" appear>
          <div class="slider-button">
            <a  href="#About" class="button-in">GET STARTED</a>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.titleOne-enter-active {
  animation: identLeft 0.8s;
}
.titleTwo-enter-active {
  animation: identRight 0.8s;
}
.titleThree-enter-active {
  animation: identLeft 0.8s;
}
.Button-enter {
  opacity: 0;
}
.Button-enter-active {
  transition: opacity 0.5s;
}
.Button-enter-to {
}

@keyframes identLeft {
  from {
    transform: translateX(-2000px);
  }
  to {
    transform: translateX(0px);
  }
}
@keyframes identRight {
  from {
    transform: translateX(+2000px);
  }
  to {
    transform: translateX(0px);
  }
}

.slider::before {
  content: "";
  height: 1030px;
  background: url(../../assets/bgtop.jpg) no-repeat top center / cover;
  position: absolute;
  left: 0;
  right: 0;
  z-index: -1;
  -webkit-filter: brightness(30%);
  -moz-filter: brightness(30%);
  -o-filter: brightness(30%);
  -ms-filter: brightness(30%);
  filter: brightness(30%);
}

.wrapper {
  height: 1030px;
}

.slider__box {
  margin: 0 auto;
  max-width: 600px;
  color: white;
  text-align: center;
  padding-top: 395px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.slider-title {
  font-family: "Montserrat Regular", sans-serif;
  font-size: 36px;
  padding-bottom: 15px;
}
.slider-bold {
  font-family: "Raleway Regular", sans-serif;
  font-weight: 900;
  font-size: 52px;
  padding-bottom: 15px;
}

.slider-text {
  padding-bottom: 50px;
}

.slider-button {
  width: 170px;
  height: 50px;
  border-radius: 5px;
  background-color: #998675;
  line-height: 50px;
  font-size: 14px;
  cursor: pointer;
}

.slider-button:hover {
  background: rgb(204, 205, 207);
}
.slider-button:active {
  background: rgb(204, 205, 207);

  a {
    color: black;
  }
}

.button-in {
  font-weight: 700;
  width: auto;
  height: auto;
  color: white;
  display: block;
}
</style>
