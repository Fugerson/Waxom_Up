<template>
  <div class="menu">
    <div class="wrapper">
      <div class="menu-container">
        <div v-for="item in postItemList" :key="item" class="menu-box">
          <img :src="item.icon" alt="img" class="menu-img" />
          <div class="menu-numeber">{{ item.number }}</div>
          <div class="menu-text">{{ item.text }}</div>
          <div class="menu-border"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppContentMenu",
  data() {
    return {
      postItemList: {
        1: {
          icon: require("@/assets/menu1.png"),
          number: "3587",
          text: "Satisfied Clients"
        },
        2: {
          icon: require("@/assets/menu2.png"),
          number: "207",
          text: "Cups of coffee"
        },
        3: {
          icon: require("@/assets/menu3.png"),
          number: "563",
          text: "Blog posts"
        },
        4: {
          icon: require("@/assets/menu4.png"),
          number: "2039",
          text: "Likes"
        },
        5: {
          icon: require("@/assets/menu5.png"),
          number: "930",
          text: "We launched"
        }
      }
    };
  }
};
</script>

<style scoped>
.menu {
  background-color: #3b2a21;
}

.menu .wrapper {
  min-height: 300px;
}

.menu .menu-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.menu-box {
  width: 168px;
  cursor: default;
  margin: 30px;
  text-align: center;
}

.menu-box img {
  width: 44px;
  height: 44px;
}

.menu-box .menu-numeber {
  margin: 30px 0 20px;
  font-size: 48px;
  color: white;
}

.menu-box .menu-text {
  color: #c7b299;
  font-size: 16px;
  margin-bottom: 30px;
}

.menu-box .menu-border {
  width: 30px;
  border-bottom: 2px solid white;
  margin: 0px auto;
}

.menu-box:hover .menu-border {
  border-color: #c7b299;
}

.menu-box:hover .menu-numeber {
  color: #c7b299;
}
</style>
