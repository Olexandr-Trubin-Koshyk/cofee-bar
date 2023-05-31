<script setup>
import AppHeader from "./components/AppHeader";
import AppFooter from "./components/AppFooter";
import AppMainInfo from "./components/AppMainInfo";
import AppMenu from "./components/AppMenu";
import AppAboutUs from "./components/AppAboutUs";
import AppContactUs from "./components/AppContactUs";
import BackgroundTriangle from "./ui/BackgroundTriangle";
</script>

<template>
  <BackgroundTriangle></BackgroundTriangle>
  <div class="contentWrapper">
    <AppHeader></AppHeader>
    <AppMainInfo></AppMainInfo>
    <AppAboutUs></AppAboutUs>
    <AppMenu></AppMenu>
    <AppContactUs></AppContactUs>
    <AppFooter></AppFooter>
  </div>
</template>

<style lang="scss">
@import "./styles/main.scss";
#app {
  width: 100vw;
  height: 100vh;
}
</style>
