<script setup>
import SidebarContents from './SidebarContents.vue'
import SidebarMid from "./SidebarMid.vue";
</script>

<template>
  <div class="sidebar">
    <header>
      <img src="../assets/common/ttl_menu.svg" alt="" id="img1">
      <img src="../assets/common/txt_contents.png" alt="" id="img2">
      <SidebarContents>
      </SidebarContents>
    </header>
    <SidebarMid>
    </SidebarMid>
    <footer>
      <img src="../assets/common/bg_en.png" alt="" id="img3">
    </footer>
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
.sidebar {
  position: fixed;
  display: flex;
  flex-direction: column;
  width: 16.6666667vw;
  height: 100vh;
  right: 0;
  border-left: 13px solid black;
  gap: 40px;
}

header {
  display: flex;
  flex-direction: column;
}

#img1, #img2 {
  position: absolute;
  right: 0;
}
#img1 {
  top: 0;
  height: 15%;
}
#img2 {
  top: 15%;
  height: 10%;
}
#img3 {
  width: 100%;
  height: 100%;
}
</style>