<template>
  <div class="multi">
    <div class="wrapper">
      <div class="multi-container">
        <div class="multi-text">
          <span>Waxom</span> Multipurpose WordPress Theme
          <p>Don't Forget to Rate the Template. Thanks so much!</p>
        </div>
        <div class="multi-button">
          <a href="#" class="multi__botton-link"><span>Purchase Now</span></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.multi {
  min-height: 150px;
  background: linear-gradient(to right, #211b19 45%, #4e3427 70%);
}

.multi .multi-container {
  display: flex;
  justify-content: space-between;
  z-index: 999;
  align-items: center;
  min-height: 150px;
}

.multi .multi-text {
  color: white;
  font-size: 28px;
  font-family: "Raleway Regular", sans-serif;
}

.multi .multi-text span {
  font-size: 28px;
  font-family: "Raleway Regular", sans-serif;
  color: #c7b299;
}

.multi .multi-text p {
  font-size: 18px;
  font-family: "Montserrat Light", sans-serif;
  color: #615855;
}

.multi-button {
  width: 170px;
  height: 50px;
  border-radius: 3px;
  background-color: #998675;
  border-bottom: 3px solid #736357;
  text-align: center;
  line-height: 50px;
}

.multi-button:hover {
  background: rgb(204, 205, 207);
  color: black;
}

.multi-button .multi__botton-link {
  display: block;
  height: 100%;
  width: 100%;
  color: white;
  font-size: 14px;
  font-family: "Raleway Extra Bold", sans-serif;
  font-weight: 600;
}
 .multi__botton-link span{
  white-space: nowrap;
}
</style>
