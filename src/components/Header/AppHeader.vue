<template>
  <header id="Home" class="header">
    <div class="wrapper">
      <div class="header__left">
        <div class="logo-box">
          <a href="#" class="logo-link">
            <img src="../../assets/logo.png" alt="logo" class="header__logo" />
            <span class="Logo-text animate__swing">Waxom</span>
          </a>
        </div>
      </div>
      <div class="header__right animate__animated ">
        <button class="Header-burger" @click="changeDisplayMenu">
          <img src="https://img.icons8.com/doodle/48/000000/menu.png" />
        </button>
        <transition
          class="wow"
          enter-active-class="animate__animated animate__fadeIn"
          leave-active-class="animate__animated animate__fadeOut"
        >
          <ul
            ref="listMenu"
            v-show="displayMenuHead || width > 633"
            class="to-be-changed header__ul"
          >
            <li
              v-for="item in menuListName"
              :key="item"
              class="header-li"
              @click="movingTo(item)"
            >
              <button :href="2" class="link-top">{{ item }}</button>
            </li>
          </ul>
        </transition>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      displayMenuHead: false,
      width: 0,
      menuListName: ["About", "Projects", "Devices", "Posts", "Contacts"]
    };
  },
  methods: {
    changeDisplayMenu() {
      this.displayMenuHead = !this.displayMenuHead;
    },
    updateWidth() {
      this.width = document.documentElement.clientWidth;
      if (this.width > 650) {
        this.displayMenuHead = false;
      }
    },
    movingTo(tr) {
      console.log(tr.toString());
      let contAbout = document.querySelector(`#ID${tr}`);
      contAbout.scrollIntoView({ block: "center", behavior: "smooth" });
    }
  },
  created() {
    window.addEventListener("resize", this.updateWidth);
    this.updateWidth();
  }
};
</script>

<style scoped lang="scss">
.header {
  position: relative;
}

.wrapper {
  min-height: 100px;
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header__left {
  float: left;
}

.logo-box {
  position: relative;
}

.logo-box .span {
  font-family: "Raleway Regular", sans-serif;
  font-size: 34px;
  color: white;
  position: absolute;
}

.header__logo {
  height: 60px;
  width: 60px;
}

.Logo-text {
  font-family: "Raleway Regular", sans-serif;
  font-size: 34px;
  color: white;
  position: absolute;
  top: 12px;
}

.Header-burger {
  display: none;
}

/* .header .wrapper .header__right .minWidth-menu .to-be-changed {
  display: none;
} */
.header__left {
  border-radius: 10px;
}
.header__ul {
  align-self: center;
  display: flex;
  flex-wrap: wrap;
  font-size: 14px;
  border-radius: 10px;
}

.header-li {
  button {
    font-weight: bold;
    text-align: center;
    display: block;
    padding: 20px 15px;
    border: none;
    color: rgb(0, 0, 0);
    background-color: rgba(255, 255, 255, 0.6);
    font-size: 26px;
  }
  button:hover {
    color: rgb(255, 255, 255);
    background-color: rgba(0, 0, 0, 0.3);
  }
}

.link-top {
  color: white;
  font-size: 16px;
}

@media screen and (max-width: 867px) {
  .header-li button {
    font-size: 22px;
    padding: 12px 8px;
  }

  .Logo-text {
    font-size: 25px;
  }
  .header__logo {
    height: 50px;
    width: 50px;
  }
}
@media screen and (max-width: 650px) {
  .header__ul {
    position: absolute;
    left: 50%;
    // margin-right: -50%;
    display: block;
    transform: translate(-50%, 30px) translateZ(0) !important;
  }
  .header-li button {
    width: 150px;
    font-size: 25px;
    padding: 10px 20px;
  }
  .header-li {
    width: 150px;
  }
  .Header-burger {
    display: block;
    width: 50px;
    height: 50px;
    align-self: center;
    cursor: pointer;
  }
}
</style>
