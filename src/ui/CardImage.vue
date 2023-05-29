<template>
  <figure class="cardImage">
    <img class="cardImage__image" :src="src" :alt="alt" />
    <figurecaption class="cardImage__priceLabel">
      <div class="cardImage__price">$ {{ price }}</div>
    </figurecaption>
  </figure>
</template>

<script>
export default {
  props: ["src", "alt", "price"],
};
</script>

<style lang="scss" scoped>
@import "../styles/main.scss";

.cardImage {
  position: relative;
  max-width: 375px;
  max-height: 375px;
  float: right;
  margin: 0;

  &__image {
    max-width: 375px;
    max-height: 375px;
    border-radius: 12px;
    clear: none;
  }

  &__priceLabel {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    bottom: 0;
    right: 0;
    width: 180px;
    height: 180px;
    border-radius: 0 0 12px 0;
    max-width: 400px;
    font-size: 26px;
    background: linear-gradient(
      to bottom right,
      transparent 0%,
      transparent 50%,
      $color-marine-blue-transparent 50%,
      $color-marine-blue 75%,
      $color-marine-blue 100%
    );
  }

  &__price {
    font-size: 36px;
    transform: rotate(-45deg);
    transform-origin: 100px -10px;
    color: $color-light-grey;
  }
}
</style>
