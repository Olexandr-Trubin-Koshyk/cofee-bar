<script setup>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import AppMainInfo from "./components/AppMainInfo.vue";
</script>

<template>
  <AppHeader></AppHeader>
  <AppMainInfo></AppMainInfo>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@import "./styles/main.scss";
#app {
  width: 100vw;
  height: 100vh;
  background-color: $bg-main-color;
}
</style>
