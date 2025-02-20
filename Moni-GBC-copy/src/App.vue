<script setup>
import Sidebar from "./components/Sidebar.vue";
import Container from "./components/Container.vue";
</script>

<template>
  <div class="total">
    <Container>

    </Container>

    <Sidebar>
    </Sidebar>
  </div>
</template>

<style>
*, body {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
.total {
  display: flex;
}
html, body {
  margin: 0;
  padding: 0;
  height: 100%;
}
</style>
