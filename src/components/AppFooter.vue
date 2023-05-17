<template>
  <div class="footer">
    <div class="footer__title">
      © {{ new Date().getFullYear() }} by CoffeeBar
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/main.scss";

.footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  @include bg-gradient-dark;
}
</style>
