<template>
  <div class="triangleBg">
    <div class="zCloser"></div>
  </div>
</template>

<style lang="scss" scoped>
@import "../styles/main.scss";
.triangleBg {
  display: flex;
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;
  justify-content: flex-end;
  height: 466px;
  width: 100%;
  background: linear-gradient(
    to top left,
    $bg-main-color 0%,
    $bg-main-color 50%,
    $color-yellow-light 50%,
    $color-yellow-light 100%
  );
}

.zCloser {
  background-color: $bg-main-color;
  width: 33vw;
}
</style>
