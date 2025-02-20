<script setup>
import icons from './icons.vue'
</script>

<template>
  <div class="menu">
    <ul class="menu-list">
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
  <div class="official">
    <div class="title">
      OFFICIAL
    </div>
    <icons>
    </icons>
  </div>
</template>

<style scoped>

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
.menu {
  padding: 14% 0 0 15%;
}
ul {
  display: flex;
  gap: 1.4rem;
  flex-direction: column;
  position: relative;
}
li {
  list-style: none;
}
a {
  text-decoration: none;
  color: #000;
  display: inline-block;
  font-family: Barlow, sans-serif;
  line-height: 1;
  position: relative; /* after的父元素是item本身，也就是a标签本身.....记得给他自己设置相对定位 */
}
.menu-list .item {
  font-weight: 900;
  position: relative;
  font-size: 1.4vw;
}
.item1:after,
.item2:after {
  content: "";
  display: block;
  position: absolute;
  background-color: #f40000;
  width: 100%;
  top: 100%;
  left: 0;
  height: 0.5vh;
}

.item2:after {
  transition: transform 0.15s ease;
  transform: scaleX(0);
  transform-origin: right;
}
.item2:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

.official {
  padding: 14% 10% 0 14%;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.official .title {
  font-weight: 900;
  font-size: 18px;
}

</style>