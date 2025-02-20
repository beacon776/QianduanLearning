<script setup>

</script>

<template>
  <div class="containerX">
    <img src="../assets/ttl_x.svg" id="img1">
    <img src="../assets/txt_follow.png" id="img2">
    <a href="https://x.com/girlsbandcry" class="item">
      <img src="../assets/bnr_x.png" id="img3">
    </a>
  </div>

</template>

<style scoped>
*, body {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.containerX {
  position: relative;
  margin: 5% 5% 8% 5%;
  border: 5px solid black;
  width: 89%;
  padding: .4166666667vw;
}
#img1 {
  position: absolute;
  width: 30%;
  left: 0;
  top: 0;
  transform: translateY(-100%);
}
#img2 {
  position: absolute;
  width: 20%;
  right: 0;
  transform: translateY(-92%);
}
#img3 {
  width: 100%;
}
.item {
  display: inline-block; /* 必须先把a设置成块级元素！！！ 喵的卡了我半天，之前犯过这个问题的！*/
  position: relative;
}
.item img {
  display: block;
  width: 100%;
}
.item::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgb(255, 0, 0);
  top: 0;
  left: 0;
  transition: opacity 0.3s ease;
  mix-blend-mode: screen;
  opacity: 0;
}

.item:hover::after,
.item:hover::before {
  opacity: 1;
}
</style>