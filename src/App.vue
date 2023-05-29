<script setup>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import AppMainInfo from "./components/AppMainInfo.vue";
import AppMenu from "./components/AppMenu";
import BackgroundTriangle from "./ui/BackgroundTriangle";
</script>

<template>
  <BackgroundTriangle></BackgroundTriangle>
  <AppHeader></AppHeader>
  <AppMainInfo></AppMainInfo>
  <AppMenu></AppMenu>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@import "./styles/main.scss";
#app {
  width: 100vw;
  height: 100vh;
}
</style>
