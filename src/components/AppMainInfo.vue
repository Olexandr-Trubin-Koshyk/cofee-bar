<template>
  <div class="mainInfo" id="main">
    <div class="mainInfo__sloganBlock">
      <div class="mainInfo__sloganTitleBlock">
        <p class="mainInfo__sloganTitle mainInfo__sloganTitle--stroke">
          Have you forgotten
        </p>
        <p class="mainInfo__sloganTitle">how good we</p>
        <p class="mainInfo__sloganTitle mainInfo__sloganTitle--stroke">
          make best aroma
        </p>
        <p class="mainInfo__sloganTitle">tastes?</p>
      </div>
      <div class="mainInfo__sloganSubInfo">
        <a href="#menu">
          <div class="mainInfo__moreAboutNav">
            <div class="mainInfo__moreAboutTitle">
              More about {{ siteTitle }}
            </div>
            <div class="mainInfo__moreAboutArrow"></div>
          </div>
        </a>
        <div class="mainInfo__buyNowBlock">
          <div class="mainInfo__priceBlock">
            <div class="mainInfo__price">$ 7,50</div>
            <div class="mainInfo__priceSubtitle">
              Get the second order in half price
            </div>
          </div>
          <div class="mainInfo__buyButton">
            <AppButton
              className="primary--2"
              buttonTitle="buy now"
              type="button"
              :handleClick="handleBuyNow"
            ></AppButton>
          </div>
        </div>
      </div>
    </div>
    <div class="mainInfo__imageBlock"></div>
  </div>
</template>

<script lang="ts">
import { inject } from "vue";
import AppButton from "../ui/AppButton.vue";

export default {
  components: {
    AppButton,
  },
  setup() {
    const siteTitle = inject("siteTitle");

    const handleBuyNow = () => console.log("click");

    return { handleBuyNow, siteTitle };
  },
};
</script>

<style scoped lang="scss">
@import "../styles/main.scss";

.mainInfo {
  position: relative;
  width: 100%;
  display: flex;
  justify-content: space-between;
  @include noSelectText;
  padding-top: 70px;
  z-index: 2;

  &__sloganBlock {
    flex-basis: 50%;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  &__sloganTitle {
    align-self: flex-end;
    text-align: end;
  }

  &__sloganTitle {
    font-weight: 400;
    font-size: 64px;
    line-height: 64px;
    letter-spacing: 15.5%;
    color: $color-marine-blue;

    &--stroke {
      color: transparent;
      -webkit-text-stroke-width: 1px;
      -webkit-text-stroke-color: $color-marine-blue;
    }
  }

  &__sloganSubInfo {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }

  &__moreAboutNav {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    gap: 10px;
    height: 220px;
    cursor: pointer;
  }

  &__moreAboutTitle {
    color: $color-marine-blue;
    font-family: Manrope, sans-serif;
    font-size: 14px;
    line-height: 18px;
    writing-mode: vertical-rl;
  }

  &__moreAboutArrow {
    background-image: url(../assets/arrow-icon.svg);
    background-size: cover;
    width: 8.5px;
    height: 50px;
    background-repeat: no-repeat;
  }

  &__buyNowBlock {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }

  &__priceBlock {
    display: flex;
    flex-direction: column;
    // align-items: center;
    width: 140px;
  }

  &__price {
    font-family: "Manrope", sans-serif;
    font-weight: 700;
    font-size: 26px;
    line-height: 36px;
  }

  &__priceSubtitle {
    font-family: "Manrope", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 150%;
  }

  &__imageBlock {
    border-radius: 20px;
    background-image: url(../assets/main-info-image.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    width: 500px;
    height: 500px;
  }
}
</style>
