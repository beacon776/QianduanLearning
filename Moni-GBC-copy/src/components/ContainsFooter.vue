<script setup>
import icons from './icons.vue'
</script>

<template>
  <div class="ContainsFooter">
    <div class="menu">
      <ul>
        <li>
          <a class="item item1" href="">
            HOME
          </a>
        </li>
        <li>
          <a class="item item2" href="">
            NEWS
          </a>
        </li>
        <li>
          <a class="item item2" href="">
            TICKET
          </a>
        </li>
      </ul>
    </div>
    <div class="title">
      <div class="title-left">
        <a href="">
          <span>TVアニメ</span>
        </a>
      </div>
      <div class="title-right">
        <span>総集編映画</span>
      </div>
    </div>
    <div class="img">
      <img src="../assets/common/bnr_footer_tv.jpg" alt="" id="img1">
    </div>
    <footer>
      <div class="left">
        <p>OFFICIAL</p>
        <icons>

        </icons>
      </div>
      <div class="right">
        <p>SHARE</p>
        <a href="">
          <span class="icon">
            <img src="../assets/X-baidilogo.png" alt="">
          </span>
        </a>
        <a href="">
          <span class="icon">
            <img src="../assets/line-logo.png" alt="">
          </span>
        </a>
        <a href="">
          <span class="icon">
            <img src="../assets/facebook-icon.png" alt="">
          </span>
        </a>
      </div>
    </footer>
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.ContainsFooter {
  width: 99.1%;
  display: flex;
  flex-direction: column;
  background-color: black;
}
.menu {
  padding: 45px 0 0 0;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
ul {
  display: flex;
  flex-direction: row;
  gap: 50px;
}
li {
  list-style: none;
}

.item {
  text-decoration: none;
  color: white;
  font-weight: 900;
  font-size: 20px;
}

.item1:after,
.item2:after {
  content: "";
  display: block;
  background-color: #f40000;
  width: 100%;
  top: 100%;
  left: 0;
  height: 0.5vh;
}

.item2:after {
  transition: transform 0.15s ease;
  transform: scaleX(0);
  transform-origin: left;
}

.item2:hover::after {
  transform: scaleX(1);
}

.title {
  position: relative;
  display: flex;
  flex-direction: row;
  gap: 6px;
  justify-content: center;
  align-items: center;
}
.title-left {
  width: 9%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: red;
  transition: opacity 0.3s ease;
}
.title-right {
  width: 9%;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 3px solid #f40000;
}

a {
  text-decoration: none;
  color: white;
}
span {
  color: white;
  font-weight: 900;
  font-size: 20px;
}

.title {
  margin: 30px 0 0 0;
  position: relative;
  width: 100%;
  display: flex;
  flex-direction: row;
  gap: 10px;
}
.title-left:hover {
  opacity: 0.7;
}
.img {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}
#img1 {
  padding: 55px 0 0 0;
  width: 30%;
  transition: opacity 0.3s ease;
  cursor: pointer;
}
#img1:hover {
  opacity: 0.7;
}
footer {
  height: 100px;
  background-color: black;
  display: flex;
  margin-bottom: 5%;
}
.left {
  display: flex;
  padding: 3% 0 0 17%;
  justify-content: flex-start;
  align-items: center;
  gap: 10px;
}
.right {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  padding: 3% 0 0 20%;
  gap: 10px;
  width: 50%;
}
p {
  color: white;
}

.icon {
  height: 33px;
  width: 33px;
}
.right img {
  height: 33px;
  width: 33px;
}
</style>