<template>
  <header class="header">
    <div class="header__triangleBg">
      <div class="header__zCloser"></div>
    </div>
    <div class="header__navMenu">
      <div class="contentWrapper">
        <div class="header__navWrapper">
          <a href="#main"><div class="header__navLogo">COFFEEBAR</div></a>
          <nav class="header__nav">
            <ul class="header__navList">
              <li class="header__navItem">
                <a class="header__navLink" href="#menu">MENU</a>
              </li>
              <li class="header__navItem">
                <a class="header__navLink" href="#about-us">ABOUT</a>
              </li>
              <li class="header__navItem">
                <a class="header__navLink" href="#contacts">CONTACTS</a>
              </li>
            </ul>
          </nav>
          <div class="header__navBasket"></div>
        </div>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
export default {};
</script>

<style lang="scss">
@import "../styles/main.scss";

.header {
  position: sticky;
  left: 0;
  top: 0;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: $bg-main-color;

  &__triangleBg {
    display: flex;
    position: absolute;
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

  &__zCloser {
    background-color: $bg-main-color;
    flex-basis: 33%;
  }

  &__navMenu {
    display: flex;
    justify-content: center;
    width: 100%;
    margin-top: 10px;
  }

  &__navList {
    display: flex;
    gap: 60px;
  }

  &__navWrapper {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__navLogo {
    color: $color-dark-grey;
    font-weight: 400;
    font-size: 36px;
    line-height: 43.2px;
    letter-spacing: 6%;
    cursor: pointer;
  }

  &__navLink {
    font-family: Manrope, sans-serif;
    color: $color-grey;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    cursor: pointer;
  }

  &__navBasket {
    background-image: url(../assets/basket-icon.svg);
    background-size: cover;
    background-repeat: no-repeat;
    width: 30px;
    height: 30px;
    cursor: pointer;
  }
}
</style>
