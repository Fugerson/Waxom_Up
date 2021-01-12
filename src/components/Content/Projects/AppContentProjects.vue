<template>
  <div id="IDProjects" class="projects">
    <div class="wrapper">
      <div class="replay">
        <div class="replay-title">Our Latest Projects.</div>
        <div class="replay-text">
          Investigationes demonstraverunt lectores legere me lius quod ii legunt
          saepius. Claritas est etiam processus dynamicus, qui sequitur
          mutationem consuetudium.
        </div>
      </div>
      <div class="projects__buttons-box">
        <div
          v-for="(item, i) in projectMenuItemList"
          :key="item"
          class="projects__button"
        >
          <a href="#" class="project__botton-link">{{
            projectMenuItemList[i]
          }}</a>
        </div>
      </div>
      <div class="projects__box-photo">
        <div
          v-for="item in projectItemList"
          :key="item"
          class="projects__photo-item"
          @click="console.log(1)"
        >
          <img :src="item.icon" alt="photo" class="projects-img" />
          <div class="project-icon">
            <div class="chain">
              <a class="priject__icon-link1" href="#"></a>
            </div>
            <div class="look">
              <a class="priject__icon-link2" href="#"></a>
            </div>
          </div>
          <div class="projects__box-text">
            <div class="projects-title">{{ item.title }}</div>
            <div class="projects-text">{{ item.text }}</div>
          </div>
        </div>
      </div>
      <div class="projects__button-bottom">
        <a href="#">LOAD MORE</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppContentProjects",
  data() {
    return {
      projectMenuItemList: [
        "All",
        "Web Design",
        "Mobile App",
        "Illustration",
        "Photography"
      ],
      projectItemList: {
        1: {
          title: "Claritas Etiam Processus",
          text: "Photography, Nature",
          icon: require("@/assets/project1.jpg")
        },
        2: {
          title: "Claritas Etiam Processus",
          text: "Photography, Nature",
          icon: require("@/assets/project2.jpg")
        },
        3: {
          title: "Claritas Etiam Processus",
          text: "Photography, Nature",
          icon: require("@/assets/project3.jpg")
        },
        4: {
          title: "Claritas Etiam Processus",
          text: "Photography, Nature",
          icon: require("@/assets/project4.jpg")
        },
        5: {
          title: "Claritas Etiam Processus",
          text: "Photography, Nature",
          icon: require("@/assets/project5.jpg")
        },
        6: {
          title: "Claritas Etiam Processus",
          text: "Photography, Nature",
          icon: require("@/assets/project6.jpg")
        }
      }
    };
  }
};
</script>

<style scoped>
.projects__buttons-box {
  display: flex;
  justify-content: center;
  padding: 40px 0;
  flex-wrap: wrap;
}

.projects__buttons-box .projects__button {
  margin: 5px 5px;
  height: 32px;
  border-radius: 3px;
  background-color: white;
  border: 1px solid #ebebeb;
  text-align: center;
  word-wrap: none;
}

.projects__buttons-box .projects__button:hover {
  background-color: #998675;
}

.projects__buttons-box .project__botton-link:hover {
  color: white;
}

.projects__buttons-box .project__botton-link {
  padding: 5px 10px;
  display: block;
  height: 100%;
  width: 100%;
  color: #8c8c8c;
  font-size: 14px;
  font-family: "Montserrat Light", sans-serif;
  font-weight: 600;
}

.projects__box-photo {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.projects__photo-item {
  width: 374px;
  position: relative;
  padding: 15px;
}

.projects__photo-item .projects-img {
  width: 100%;
  height: 300px;
  vertical-align: middle;
}
.projects__photo-item .projects__box-text {
  padding: 30px;
  background-color: #fbfaf8;
  line-height: 30px;
}

.projects__photo-item .projects-title {
  color: #c7b299;
  font-size: 20px;
}

.projects__photo-item .projects-text {
  color: #d1d1d1;
  font-size: 14px;
}

.projects__photo-item:hover .projects-img {
  -webkit-filter: brightness(30%);
  -moz-filter: brightness(30%);
  -o-filter: brightness(30%);
  -ms-filter: brightness(30%);
  filter: brightness(30%);
}

.projects__photo-item:hover .project-icon {
  position: absolute;
  width: 25px;
  height: 25px;
}

.projects__photo-item:hover .chain {
  background-image: url(../../../assets/chain.png);
  left: 125px;
  bottom: 220px;
  position: absolute;
  width: 25px;
  height: 25px;
}

.projects__photo-item:hover .look {
  background-image: url(../../../assets/look.png);
  left: 180px;
  bottom: 220px;
  position: absolute;
  width: 25px;
  height: 25px;
}

.projects__photo-item:hover .priject__icon-link1 {
  display: block;
  width: 25px;
  height: 25px;
  cursor: pointer;
}

.projects__photo-item:hover .priject__icon-link2 {
  display: block;
  width: 25px;
  height: 25px;
}

.projects__photo-item:hover .projects__box-text {
  background-color: #362f2d;
}

.projects__photo-item:hover .projects-title {
  color: #ffffff;
}

.projects__photo-item:hover .projects-text {
  color: #c7b299;
}

.projects__button-bottom {
  width: 170px;
  height: 50px;
  background-color: #998675;
  border-radius: 4px;
  border-bottom: 3px solid #736357;
  text-align: center;
  line-height: 50px;
  margin: 40px auto 80px;
}

.projects__button-bottom:hover {
  background: rgb(204, 205, 207);
  color: black;
}

.projects__button-bottom a {
  display: block;
  width: 100%;
  height: 100%;
  font-size: 14px;
  color: white;
  font-family: "Raleway Extra Bold", sans-serif;
}
@media screen and (max-width: 780px) {
  .projects__photo-item .projects-img {
    width: 100%;
    height: auto;
  }
}
@media screen and (max-width: 480px) {
  .projects__photo-item:hover .chain {
    display: none;
  }

  .projects__photo-item:hover .look {
    display: none;
  }
}
</style>
