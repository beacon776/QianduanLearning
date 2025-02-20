<script setup>
import ContainerNews from "../components/ContainerNews.vue";
import ContainerX from "../components/ContainerX.vue";
import ContainsFooter from "../components/ContainsFooter.vue";
</script>

<template>
  <div class="container">
    <header>
      <div class="firstview">
        <img src="../assets/img_kv-movie-01.webp" id="img1">
      </div>
    </header>
    <main>
      <ContainerNews>
      </ContainerNews>
      <ContainerX>
      </ContainerX>
    </main>
    <footer>
      <ContainsFooter>
      </ContainsFooter>
    </footer>
  </div>

</template>

<style scoped>
*, body{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
main {
  margin: 0;
  padding: 0;
}
.container {
  margin: 0;
  padding: 0;
  width: 84%;
  display: flex;
  flex-direction: column;
}
.firstview {
  width: 99.1%;
}
#img1 {
  display: block;
  width: 100%;
}
</style>