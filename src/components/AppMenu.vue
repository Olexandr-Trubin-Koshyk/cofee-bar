<script setup>
import MenuCard from "../ui/MenuCard";
</script>

<template>
  <div class="menu" id="menu">
    <div class="contentWrapper">
      <div class="menu__titlesBlock">
        <span class="menu__title">CoffeeBar</span>
        <span class="menu__title menu__title--stroke">Menu</span>
      </div>
      <div class="menu__items">
        <ul class="menu__itemsList">
          <li class="menu__item" v-for="item in items" :key="item.id">
            <MenuCard
              :title="item.title"
              :subTitle="item.subTitle"
              :imgSrc="item.imgSrc"
              :imgDescription="item.imgDescription"
              :itemPrice="item.itemPrice"
            />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: "1" + new Date(),
          title: "Test title 1",
          subTitle: "menu subtitle lorem ipsun test test test test !",
          imgSrc:
            "https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg",
          imgDescription: "this is image1 description",
          itemPrice: "7.50",
        },
        {
          id: "2" + new Date(),
          title: "Test title 2",
          subTitle: "menu subtitle lorem ipsun test test test test !",
          imgSrc:
            "https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg",
          imgDescription: "this is image2 description",
          itemPrice: "7.50",
        },
        {
          id: "3" + new Date(),
          title: "Test title 3",
          subTitle: "menu subtitle lorem ipsun test test test test !",
          imgSrc:
            "https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg",
          imgDescription: "this is image3 description",
          itemPrice: "7.50",
        },
        {
          id: "4" + new Date(),
          title: "Test title 4",
          subTitle: "menu subtitle lorem ipsun test test test test !",
          imgSrc:
            "https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg",
          imgDescription: "this is image1 description",
          itemPrice: "9.99",
        },
        {
          id: "5" + new Date(),
          title: "Test title 5",
          subTitle: "menu subtitle lorem ipsun test test test test !",
          imgSrc:
            "https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg",
          imgDescription: "this is image2 description",
          itemPrice: "3.99",
        },
        {
          id: "6" + new Date(),
          title: "Test title 6",
          subTitle:
            "menu subtitle lorem ipsun test test test test ! menu subtitle lorem ipsun test test test test subtitle lorem ipsun test test test test !",
          imgSrc:
            "https://as2.ftcdn.net/v2/jpg/01/39/41/31/500_F_139413171_2hAZi8ia6E054vO3ULfG6SY048RWTymM.jpg",
          imgDescription: "this is image3 description",
          itemPrice: "7.50",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/main.scss";
.menu {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 80px;
  padding-top: 70px;

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

  &__items {
    width: 100%;
  }

  &__itemsList {
    padding: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
}
</style>
