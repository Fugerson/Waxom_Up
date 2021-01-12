<template>
  <footer id="IDContacts" class="footer">
    <div class="wrapper">
      <div class="footer-box">
        <div class="footer__left-box footer-boxin">
          <div class="footer__left-left">
            <div class="footer__box-logo">
              <a href="#" class="logo-link">
                <img
                  src="../../assets/logo.png"
                  alt="logo"
                  class="footer__logo"
                />
                <span class="footer-text">Waxom</span>
              </a>
            </div>
            <div class="footer__left__left__text">
              Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam
              nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam
              erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci
              suscipit lobortis claritatem.
            </div>
            <div>
              <a href="#" class="footer__left__left-bottom">Read More</a>
            </div>
          </div>
          <div class="footer__left-right">
            <div class="footer-title">Recent Posts</div>
            <div
              v-for="item in footerCommentsItemList"
              :key="item"
              class="footer__left__right-box"
            >
              <div class="footer__left__right-colendar">
                {{ item.calendarData }}
              </div>
              <div class="footer__left__right-text">
                {{ item.textComment }}
              </div>
            </div>
          </div>
        </div>
        <div class="footer__right-box footer-boxin">
          <div class="footer__right-left">
            <div class="footer-title">Our Twitter</div>
            <div class="footer__left__right-box">
              <div class="footer__left__right-text">
                <a href="#">@footer</a> Cum soluta nobis eleifend option congue
                nihil imperdiet doming
              </div>
              <div class="footer__left__right-colendar">3 mins ago</div>
            </div>
            <div class="footer__left__right-box">
              <div class="footer__left__right-text pd-text">
                Mirum est <a href="#">#envato</a> notare quam littera gothica,
                quam nunc putamus parum anteposuerit litterarum
              </div>
              <div class="footer__left__right-colendar">5 hours ago</div>
            </div>
            <div class="footer__left__right-box">
              <div class="footer__left__right-text pd-text">
                Soluta nobis option
                <a href="#" class="footer__lr-link">bit.ly/1Hniso7</a>
              </div>
              <div class="footer__left__right-colendar">20 days ago</div>
            </div>
          </div>
          <div class="footer__right-right">
            <div class="footer-title">Dribbble Widget</div>
            <div class="footer__photo-box">
              <div
                v-for="item in footerPhotoItemList"
                :key="item"
                class="footer__right-photo"
              >
                <img :src="item.icon" alt="" class="footer-photo" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <AppFooterBottom />
  </footer>
</template>

<script>
import AppFooterBottom from "./AppFooterBottom";

export default {
  name: "AppFooter",
  components: {
    AppFooterBottom
  },
  data() {
    return {
      footerCommentsItemList: {
        1: {
          calendarData: "September 22.2020",
          textComment:
            "Claritas est etiam processus dynamicus, qui sequitur mutationemper seacula quarta decima"
        },
        2: {
          calendarData: "October 08.2020",
          textComment:
            "Diam nonummy nibh euismod tincidunt ut laoreet dolore magna"
        },
        3: {
          calendarData: "November 28.2020",
          textComment:
            "Lorem ipsum dolor sit amet, consectetuer adipiscing elit"
        }
      },
      footerPhotoItemList: {
        1: {
          icon: require("@/assets/waxom-photo1.jpg")
        },
        2: {
          icon: require("@/assets/waxom-photo2.jpg")
        },
        3: {
          icon: require("@/assets/waxom-photo3.jpg")
        },
        4: {
          icon: require("@/assets/waxom-photo4.jpg")
        }
      }
    };
  }
};
</script>

<style scoped>
.footer {
  background-color: #191919;
  min-height: 500px;
}

.footer .wrapper {
  min-height: 500px;
}

.footer .footer-box {
  display: flex;
  padding-top: 70px;
}

.footer .footer__left-box,
.footer__right-box {
  display: flex;
}

.footer__left {
  float: left;
}

.footer__box-logo {
  position: relative;
}

.footer__logo {
  height: 60px;
  width: 60px;
}

.footer-text {
  font-family: "Raleway Regular", sans-serif;
  font-size: 34px;
  color: white;
  position: absolute;
  top: 12px;
}

.footer__left-left {
  max-width: 280px;
}

.footer__left__left__text {
  font-size: 14px;
  font-family: "Montserrat Light", sans-serif;
  color: #555555;
  padding: 30px 0 40px;
}

.footer__left__left-bottom {
  color: #d1d1d1;
  background: url(../../assets/arrow.png) no-repeat right;
  padding-right: 15px;
}

.footer__left-right {
  padding: 0 40px;
  max-width: 280px;
}

.footer__left-right .footer__left__right-text {
  color: #555555;
  font-size: 14px;
  font-family: "Montserrat Light", sans-serif;
}

.footer__left__right-box {
  padding-bottom: 10px;
  border-bottom: 1px solid #252525;
}

.footer__left__right-box:last-child {
  padding-bottom: 0;
  border-bottom: 0px solid #252525;
}

.footer__left__right-colendar {
  color: #363636;
  font-size: 12px;
  font-family: "Montserrat Light", sans-serif;
  padding: 10px 0;
}

.pd-text {
  padding-top: 20px;
}

.footer__lr-link {
  color: #959595;
}

.footer-title {
  font-size: 24px;
  font-family: "Raleway Extra Bold", sans-serif;
  color: white;
  margin-bottom: 30px;
}

.footer__right-left {
  padding: 0 25px;
  max-width: 280px;
}

.footer__right-left .footer__left__right-text {
  color: #555555;
  font-size: 14px;
  font-family: "Montserrat Light", sans-serif;
}

.footer__right-left .footer__left__right-text a {
  color: #00bff3;
}

.footer__right-left .footer__left__right-text span:nth-child(3) {
  color: #959595;
}

.footer__right-right {
  max-width: 280px;
}

.footer__right-right .footer__photo-box {
  display: flex;
  flex-wrap: wrap;
  max-width: 280px;
}

.footer__right-right .footer-photo {
  margin: 5px;
  width: 130px;
  height: 100px;
}
@media screen and (max-width: 700px) {
  .footer .footer-box {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  .footer-boxin {
    padding-top: 30px;
    flex-wrap: wrap;
    justify-content: center;
  }
  .footer__left-right,
  .footer__right-left {
    padding: 15px 0 0 0;
  }
  .footer .footer-box {
    padding-top: 0;
  }
}
@media screen and (max-width: 340px) {
  .footer-title {
    text-align: center;
  }
  .footer__photo-box {
    justify-content: center;
  }
}
</style>
