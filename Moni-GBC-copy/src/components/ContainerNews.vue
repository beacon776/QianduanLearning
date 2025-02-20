<script setup>

</script>

<template>
  <div class="containerNews">
    <div class="content">
      <img src="../assets/common/ttl_news.svg" alt="" id="img1">
      <img src="../assets/common/txt_check.png" alt="" id="img2">
      <ul>
        <li class="item">
          <a class="item-link" href="">
            <img src="../assets/GBC_b2.png" alt="" class="img3">
            <p class="content2">3/15(土)トゲナシトゲアリ 1st ONE-MAN LIVE “薄明の序奏” 【LIVE ZOUND】上映会 実施決定！</p>
            <p class="time">2025.02.14</p>
          </a>
        </li>
        <li class="item">
          <a class="item-link" href="">
            <img src="../assets/GBC_b2.png" alt="" class="img3">
            <p class="content2">ガルクラ展名古屋会場・福岡会場の開催が決定！イラストレーターコラボも！</p>
            <p class="time">2025.02.14</p>
          </a>
        </li>
        <li class="item">
          <a class="item-link" href="">
            <img src="../assets/HP映画情報.png" alt="" class="img3">
            <p class="content2">ガールズバンドクライ劇場版総集編ティザービジュアル公開！前売券は3/20(木・祝）発売！</p>
            <p class="time">2025.02.07</p>
          </a>
        </li>
        <li class="item">
          <a class="item-link" href="">
            <img src="../assets/0207日本武道館告知画像-1024x576.jpg" alt="" class="img3">
            <p class="content2">トゲナシトゲアリ LIVE in 日本武道館、 2025年9月23日（火・祝）開催決定！</p>
            <p class="time">2025.02.07</p>
          </a>
        </li>
      </ul>
      <div class="more">
        <a href="">MORE</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.containerNews {
  display: flex;
  flex-direction: column;
}

#img1 {
  left: 0;
  top: 0;
  position: absolute;
  width: 30%;
  transform: translateY(-100%);
}
#img2 {
  position: absolute;
  width: 20%;
  right: -0%;
  top: 0;
  transform: translateY(-100%);
}
.content {
  position: relative;
  border: 5px solid black;
  margin: 7% 6% 2% 6%;
  display: flex;
  flex-direction: row;
  padding-bottom: 6%;
}
ul {
  padding: 30px;
  position: relative;
  display: flex;
  flex-direction: row;
  gap: 15px;
  justify-content: center;
}
li {
  list-style: none;
  display: flex;
  flex-direction: column;
}
.item {
  width: 23%;
}
.item-link {
  position: relative;
  width: 100%;
  color: black;
  text-decoration: none;
  transition: color 0.1s, background-color 0.1s;
  background-color: white;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  height: 100%;
}
.item-link p {
  margin: 0;
}
.item-link:hover {
  color: red;
}
.item-link:hover::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(250, 0, 0, 0.5);
  z-index: -1;
}
.item-link:hover .img3 {
  opacity: 0.3;
}
.time {
  color: #f40000;
  margin-top: 10px;
  text-align: left;
  font-size: 14px;
}
.img3 {
  width: 100%;
  transition: opacity 0.1s;
}
.item {
  background-color: white;
}
.more {
  position: absolute;
  width: 10%;
  height: 15%;
  right: 0;
  bottom: 5%;
  background-color: red;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  transition: background-color 0.25s;
}
.more a {
  text-decoration: none;
  color: white;
  font-weight: 700;
  font-size: 21px;
  z-index: 1;
}
.more::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: black;
  transition: left 0.25s ease-out;
}
.more:hover {
  background-color: black;
}
.more:hover::before {
  left: 100%;
}
.content2 {
  height: 40%;
  padding-bottom: 90px;
  font-size: 16px;
  font-weight: 900;
}
.time {
  position: absolute;
  font-size: 16px;
  font-weight: 900;
  bottom: 30px;
}
</style>