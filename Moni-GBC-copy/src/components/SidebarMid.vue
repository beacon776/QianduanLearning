<script setup>

</script>

<template>
  <div class="sidebarMid">
    <div class="sidebarMid-left">
      <a href="">
        <span>TVアニメ</span>
      </a>
    </div>
    <div class="sidebarMid-right">
      <span>総集編映画</span>
    </div>
  </div>
</template>

<style scoped>
.sidebarMid {
  border-top: 13px solid black;
  border-bottom: 13px solid black;
  position: relative;
  width: 100%;
  display: flex;
  flex-direction: row;
  gap: 20px;
}

.sidebarMid-left {
  height: 60px;
  width: 48%;
  border-right: 11px solid black;
  background-color: #f40000;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: opacity 0.2s ease;
  cursor: pointer;
}
.sidebarMid-left:hover {
  opacity: 0.6;
}
.sidebarMid-right {
  height: 60px;
  width: 40%;
  display: flex;
  justify-content: center;
  align-items: center;
}
a {
  text-decoration: none;
  color: white;
}
span {
  font-weight: 900;
  font-size: 18px;
}
</style>