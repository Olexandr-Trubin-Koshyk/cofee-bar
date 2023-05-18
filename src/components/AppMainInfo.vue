<script setup>
import VButton from "../ui/VButton";
</script>

<template>
  <div class="mainInfo">
    <div class="contentWrapper">
      <div class="mainInfo__infoBlock">
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
            <div class="mainInfo__moreAboutNav">
              <div class="mainInfo__moreAboutTitle">More about CoffeeBar</div>
              <div class="mainInfo__moreAboutArrow"></div>
            </div>
            <div class="mainInfo__buyNowBlock">
              <div class="mainInfo__priceBlock">
                <div class="mainInfo__price">$ 7,50</div>
                <div class="mainInfo__priceSubtitle">
                  Get the second order in half price
                </div>
              </div>
              <div class="mainInfo__buyButton">
                <VButton
                  className="primary--2"
                  buttonTitle="buy now"
                  type="button"
                  :handleClick="() => console.log('click')"
                ></VButton>
              </div>
            </div>
          </div>
        </div>
        <div class="mainInfo__imageBlock"></div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "../styles/main.scss";

.mainInfo {
  position: relative;
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 70px;
  height: 100px;

  &__infoBlock {
    display: flex;
    justify-content: space-between;
    @include noSelectText;
  }

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
    height: 200px;
    cursor: pointer;
  }

  &__moreAboutTitle {
    color: $color-marine-blue;
    font-family: Manrope, sans-serif;
    font-size: 12px;
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
