<script setup>
import MenuCard from "../ui/MenuCard";
</script>

<template>
  <div class="menu">
    <div class="contentWrapper">
      <div class="menu__titlesBlock">
        <span class="menu__title">CoffeeBar</span>
        <span class="menu__title menu__title--stroke">Menu</span>
      </div>
      <div class="menu__items">
        <ul class="menu__itemsList">
          <li class="menu__item">
            <MenuCard
              title="Test title 1"
              subTitle="menu subtitle lorem ipsun test test test test !"
              imgSrc="https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg"
              imgDescription="this is image1 description"
            />
          </li>
          <li class="menu__item">
            <MenuCard
              title="Test title 2"
              subTitle="menu subtitle lorem ipsun test test test test !"
              imgSrc="https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg"
              imgDescription="this is image2 description"
            />
          </li>
          <li class="menu__item">
            <MenuCard
              title="Test title 3"
              subTitle="menu subtitle lorem ipsun test test test test !"
              imgSrc="https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg"
              imgDescription="this is image3 description"
            />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../styles/main.scss";
.menu {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 150px;

  &__title {
    font-family: "Bebas Neue", sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 58px;
    line-height: 70px;
    letter-spacing: 0.155em;
    color: $color-marine-blue;

    &--stroke {
      color: transparent;
      -webkit-text-stroke-width: 1px;
      -webkit-text-stroke-color: $color-marine-blue;
    }
  }
}
</style>
