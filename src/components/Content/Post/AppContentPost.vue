<template>
  <div id="IDPosts" class="post">
    <div class="wrapper">
      <div class="replay">
        <div class="replay-title">Recent Posts.</div>
        <div class="replay-text">
          Investigationes demonstraverunt lectores legere me lius quod ii legunt
          saepius. Claritas est etiam processus dynamicus, qui sequitur
          mutationem consuetudium.
        </div>
      </div>
      <div class="post-container">
        <div class="post__photo-item" v-for="item in postItemList" :key="item">
          <img :src="item.icon" alt="photo" class="post-img" />
          <div class="post-calendar">
            <div class="post-day">{{ item.day }}</div>
            <div class="post-month">{{ item.month }}</div>
          </div>
          <div class="post__box-text">
            <div class="post-title">{{ item.title }}</div>
            <div class="post-text">
              {{ item.text }}
            </div>
            <div class="post-button">
              <a href="#" class="post__button-link">Read More </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppContentPost",
  data() {
    return {
      postItemList: {
        1: {
          day: "23",
          month: "sep",
          icon: require("@/assets/post1.jpg"),
          title: "Claritas Etiam Processus",
          text: "Photography, Nature"
        },
        2: {
          day: "26",
          month: "sep",
          icon: require("@/assets/post2.jpg"),
          title: "Claritas Etiam Processus",
          text: "Photography, Nature"
        },
        3: {
          day: "1",
          month: "oсt",
          icon: require("@/assets/post3.jpg"),
          title: "Claritas Etiam Processus",
          text: "Photography, Nature"
        }
      }
    };
  }
};
</script>

<style scoped>
.post {
  min-height: 750px;
}

.post .replay {
  margin-bottom: 30px;
}

.post .post-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.post-container .post__photo-item {
  width: 350px;
  position: relative;
  margin: 15px;
}

.post-container .post-img {
  vertical-align: middle;
  cursor: pointer;
}

.post-calendar {
  width: 50px;
  height: 60px;
  border-radius: 5px;
  position: absolute;
  left: 20px;
  top: 20px;
  text-align: center;
}

.post-calendar .post-day {
  line-height: 38px;
  width: 50px;
  height: 35px;
  background-color: #363636;
  font-size: 24px;
  color: white;
}

.post-calendar .post-month {
  line-height: 26px;
  width: 50px;
  height: 25px;
  background-color: #252525;
  font-size: 12px;
  color: white;
}

.post__box-text {
  padding: 30px;
  background-color: #fbfaf8;
  line-height: 40px;
}

.post__box-text .post-title {
  color: #555555;
  font-size: 20px;
}

.post__box-text .post-text {
  color: #8c8c8c;
  font-size: 14px;
  line-height: 20px;
}

.post__box-text .post__button-link {
  color: #c7b299;
  background: url(../../../assets/arrow.png) no-repeat right;
  padding-right: 15px;
}

.post__photo-item:hover .post-img {
  -webkit-filter: brightness(30%);
  -moz-filter: brightness(30%);
  -o-filter: brightness(30%);
  -ms-filter: brightness(30%);
  filter: brightness(30%);
}

.post__photo-item:hover .post-icon {
  position: absolute;
  width: 25px;
  height: 25px;
}

.post__photo-item:hover .post__icon-link1 {
  display: block;
  width: 25px;
  height: 25px;
  cursor: pointer;
}

.post__photo-item:hover .post__icon-link2 {
  display: block;
  width: 25px;
  height: 25px;
}

.post__photo-item:hover .post__box-text {
  background-color: #362f2d;
}

.post__photo-item:hover .post-title {
  color: #ffffff;
}

.post__photo-item:hover .post-text {
  color: #c7b299;
}

.post__photo-item:hover .post-day {
  background-color: #c7b299;
}

.post__photo-item:hover .post-month {
  background-color: #a48d72;
}
</style>
