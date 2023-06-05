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

<script lang="ts">
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import AppMainInfo from "./components/AppMainInfo.vue";
import AppMenu from "./components/AppMenu.vue";
import AppAboutUs from "./components/AppAboutUs.vue";
import AppContactUs from "./components/AppContactUs.vue";
import BackgroundTriangle from "./ui/BackgroundTriangle.vue";
import { provide } from "vue";

export default {
  components: {
    AppHeader,
    AppFooter,
    AppMainInfo,
    AppMenu,
    AppAboutUs,
    AppContactUs,
    BackgroundTriangle,
  },
  setup() {
    provide("siteTitle", "CoffeeBar");
  },
};
</script>

<style lang="scss">
@import "./styles/main.scss";
#app {
  width: 100vw;
  height: 100vh;
}
</style>
