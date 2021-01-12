<template>
  <div class="partners">
    <div class="wrapper">
      <div class="partners__itam-box">
        <div class="wrapper__partners-item">
          <div
            v-for="item in parthnersItemList"
            :key="item"
            class="partners-item"
          >
            <a href="#">
              <img :src="item.icon" alt="partners" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppContentPartners",
  data() {
    return {
      parthnersItemList: {
        1: {
          icon: require("@/assets/partners-1.png")
        },
        2: {
          icon: require("@/assets/partners-2.png")
        },
        3: {
          icon: require("@/assets/partners-3.png")
        },
        4: {
          icon: require("@/assets/partners-4.png")
        }
      }
    };
  }
};
</script>

<style scoped>
.partners {
  background: url(../../../assets/bg-partners.jpg) center;
  background-size: cover;
  min-height: 500px;
}

.partners__itam-box {
  min-height: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.partners__itam-box .partners-item {
  max-width: 100%;
  margin: 50px 30px 20px 30px;
}

.wrapper__partners-item {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.partners::before {
  content: "";
  background: url(../../../assets/bg-partners.jpg) center;
  background-size: cover;
  min-height: 500px;
  position: absolute;
  left: 0;
  right: 0;
  z-index: -1;
  -webkit-filter: brightness(40%);
  -moz-filter: brightness(40%);
  -o-filter: brightness(40%);
  -ms-filter: brightness(40%);
  filter: brightness(40%);
}
</style>
