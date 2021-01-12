<template>
  <div id="app">
    <AppHeader />
    <AppSlider />
    <AppContent />
    <AppFooter />
  </div>
</template>

<script>
import "./assets/animate.css";

import AppHeader from "./components/Header/AppHeader";
import AppSlider from "./components/slider/AppSlider";
import AppFooter from "./components/Footer/AppFooter";
import AppContent from "./components/Content/AppContent";

export default {
  name: "App",
  components: {
    AppHeader,
    AppSlider,
    AppContent,
    AppFooter
  }
};
</script>
<style>
body,
div,
dl,
dt,
dd,
ul,
li,
h1,
h2,
h3,
h4,
h5,
h6,
pre,
code,
form,
fieldset,
input,
textarea,
p,
blockquote,
th,
td {
  margin: 0;
  padding: 0;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

fieldset,
img,
abbr {
  border: 0;
}

address,
caption,
cite,
code,
dfn,
em,
strong,
th,
var {
  font-style: normal;
  font-weight: normal;
}

ul li {
  list-style: none;
}

caption,
th {
  text-align: left;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: 100%;
  font-weight: normal;
}

sup {
  vertical-align: text-top;
}

sub {
  vertical-align: text-bottom;
}

input,
textarea,
select {
  font-family: inherit;
  font-size: inherit;
  font-weight: inherit;
}

legend {
  color: #000;
}

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section,
main {
  display: block;
}

img {
  width: 100%;
  height: auto;
}

* {
  margin: 0;
  padding: 0;
  outline: none;
  box-sizing: border-box;
}

.wrapper {
  max-width: 1230px;
  margin: 0 auto;
  padding-left: 30px;
  padding-right: 30px;
}

body {
  font-family: "Montserrat Light", sans-serif;
  font-size: 16px;
}
a {
  text-decoration: none;
}

.replay {
  text-align: center;
  padding-top: 80px;
  max-width: 780px;
  margin: 0 auto;
}

.replay .replay-title {
  font-family: "Raleway Semibold", sans-serif;
  font-size: 30px;
  color: #555555;
  padding-bottom: 30px;
}

.replay .replay-text {
  font-size: 16px;
  color: #8c8c8c;
}

@media screen and (min-width: 700px) {
  .header .wrapper .photo-left {
    width: 370px;
    height: 200px;
  }
  .header .wrapper .photo-center {
    width: 370px;
    height: 280px;
  }
  .header .wrapper .photo-right {
    width: 370px;
    height: 200px;
  }
}

@media screen and (max-width: 920px) {
  .wrapper {
    padding-left: 15px;
    padding-right: 15px;
  }
}

@media screen and (max-width: 700px) {
  .waxom .waxom-box {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  .waxom__right-box {
    padding-top: 30px;
  }
}

@media screen and (max-width: 1100px) {
  .header .wrapper {
    display: flex;
  }
}

@media screen and (max-width: 620px) {
  .about__item-box {
    display: block;
  }
}

@media screen and (max-width: 520px) {
  .mobile .mobile__photo {
    display: none;
  }
  .wrapper__partners-item {
    display: block;
  }
  .multi__botton-link span {
    font-size: 10px;
  }
}

@media screen and (min-width: 750px) {
  .waxom__photo-box {
    flex-wrap: wrap;
  }
}
</style>
