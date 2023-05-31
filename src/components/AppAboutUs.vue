<template>
  <div class="aboutUs" id="about-us">
    <div class="aboutUs__title">About Us</div>
    <div class="aboutUs__mainInfo">
      <div class="aboutUs__interiorImage"></div>
      <div class="aboutUs__info">
        <div class="aboutUs__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam
          sollicitudin lobortis arcu, eget faucibus sapien vestibulum et. Fusce
          nec consectetur mi. In sit amet sem sed felis consectetur vulputate ut
          ut enim. Nunc dui lacus, condimentum ut arcu ut, aliquam facilisis
          purus. Nunc ut nulla quis elit convallis pulvinar non a velit. Class
          aptent taciti sociosqu ad litora torquent per conubia nostra, per
          inceptos himenaeos. Mauris tristique vehicula felis eget pretium.
        </div>
        <div class="aboutUs__navBlock">
          <div></div>
          <a href="#menu" class="aboutUs__link">
            <div class="aboutUs__moreAboutNav">
              <div class="aboutUs__moreAboutTitle">Contact Us</div>
              <div class="aboutUs__moreAboutArrow"></div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/main.scss";

.aboutUs {
  display: flex;
  gap: 24px;
  flex-direction: column;
  margin-top: 80px;
  padding-top: 70px;

  &__title {
    @include titleBlack;
  }

  &__mainInfo {
    display: flex;
    justify-content: space-between;
  }

  &__interiorImage {
    width: 650px;
    height: 600px;
    background-size: cover;
    border-radius: 12px;
    background-repeat: no-repeat;
    background-image: url(../assets/coffe-bar-interior.jpg);
  }

  &__info {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  &__description {
    width: 450px;
    font-size: 24px;
    letter-spacing: 0.1em;
    text-align: justify;
  }

  &__navBlock {
    display: flex;
    justify-content: space-between;
  }

  &__moreAboutNav {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    gap: 10px;
    height: 200px;
    width: 20px;
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

  &__link {
    margin: 0;
  }
}
</style>
