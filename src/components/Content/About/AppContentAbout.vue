<template>
  <section id="IDAbout" class="about">
    <div class="wrapper">
      <div class="about-box">
        <a
          href="#"
          class="about__item hover"
          v-for="(item, i) in infoOnject"
          :key="item"
        >
          <div :class="`about_item-imgALL about__item-img${i}`"></div>
          <div class="about__item-title title-hover">{{ item.title }}</div>
          <div class="about__item-text">
            {{ item.text }}
          </div>
          <div class="about__item-border border-hover"></div>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "footer-title",
  data() {
    return {
      infoOnject: {
        "1": {
          title: "Web & App Design",
          text:
            "Nam liber tempor cum soluta nobis eleifend option congue nihilimperdiet doming id quod mazim"
        },
        "2": {
          title: "Development",
          text:
            "Nam liber tempor cum soluta nobis eleifend option congue nihilimperdiet doming id quod mazim"
        },
        "3": {
          title: "Customization",
          text:
            "Nam liber tempor cum soluta nobis eleifend option congue nihilimperdiet doming id quod mazim"
        },
        "4": {
          title: "Marketing",
          text:
            "Nam liber tempor cum soluta nobis eleifend option congue nihilimperdiet doming id quod mazim"
        }
      }
    };
  },
  computed: {
    imgAdd() {
      return {};
    }
  }
};
</script>

<style scoped>
.about {
  padding-top: 80px;
}

.about-box {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.about__item-box {
  display: flex;
}

.about__item {
  margin: 10px;
  max-width: 270px;
  color: #8c8c8c;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.about__item-title {
  font-family: "Raleway Regular", sans-serif;
  font-size: 22px;
  padding: 30px 0 20px;
}
.about__item-text {
  font-size: 14px;
  padding-bottom: 30px;
}
.about_item-imgALL {
  background-repeat: no-repeat;
  width: 50px;
  height: 50px;
  margin: 0 auto;
}
.hover:hover .title-hover {
  color: #c7b299;
}
.hover:hover .border-hover {
  border-color: #c7b299;
  border-bottom: 3px solid #c7b299;
}
.about__item-border {
  width: 70px;
  border-bottom: 3px solid #f1eee9;
}
.about__item-img1 {
  background-image: url(../../../assets/top-pan1.png);
}

.about__item-img2 {
  background-image: url(../../../assets/top-square2.png);
}

.about__item-img3 {
  background-image: url(../../../assets/top-ring3.png);
}

.about__item-img4 {
  background-image: url(../../../assets/top-bag4.png);
}
.hover:hover .about__item-img1 {
  background-image: url(../../../assets/top-hover1.png);
}
.hover:hover .about__item-img2 {
  background-image: url(../../../assets/top-hove2r.png);
}

.hover:hover .about__item-img3 {
  background-image: url(../../../assets/top-hover3.png);
}

.hover:hover .about__item-img4 {
  background-image: url(../../../assets/top-hover4.png);
}
</style>
