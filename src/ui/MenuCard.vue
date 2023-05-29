<template>
  <div class="card">
    <img class="card__image" :src="imgSrc" :alt="imgDescription" />
    <div class="card__title">{{ title }}</div>
    <div class="card__subTitle">{{ subTitle }}</div>
  </div>
</template>

<script>
export default {
  props: ["imgSrc", "title", "subTitle", "imgDescription"],
};
</script>

<style lang="scss" scoped>
@import "../styles/main.scss";
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 20px;
  width: 100%;
  max-width: 375px;
  margin-bottom: 24px;

  &__image {
    max-width: 375px;
    max-height: 375px;
    border-radius: 12px;
  }

  &__title {
    font-family: "Bebas Neue", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 24px;
    letter-spacing: 0.155em;
    text-transform: uppercase;
    color: $color-black;
  }

  &__subTitle {
    font-family: "Manrope";
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 150%;
    color: $color-grey;
  }
}
</style>
