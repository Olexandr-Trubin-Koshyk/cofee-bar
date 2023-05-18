<template>
  <button
    class="mainButton"
    :class="className"
    :type="type"
    @click="handleClick"
  >
    <span class="mainButton__title title">{{ buttonTitle }}</span>
    <div class="mainButton__arrow arrow"></div>
  </button>
</template>

<script>
export default {
  props: ["className", "type", "handleClick", "buttonTitle"],
};
</script>

<style lang="scss" scoped>
@import "../styles/main.scss";
.mainButton {
  padding: 14px;
  border: 1px solid;
  display: flex;
  gap: 10px;
  justify-content: center;
  align-items: center;
  min-width: 200px;
  cursor: pointer;
  transition: border-color, background-color 0.2s ease-in-out;

  &__title {
    font-family: "Manrope", sans-serif;
    font-weight: 600;
    font-size: 14px;
    line-height: 14px;
    text-transform: uppercase;
    transition: color 0.2s ease-in-out;
  }

  &__arrow {
    width: 26px;
    height: 8px;
    -webkit-mask-image: url(../assets/arrow-button-icon.svg);
    mask-image: url(../assets/arrow-button-icon.svg);
    transition: background-color 0.2s ease-in-out;
  }
}

.primary--1 {
  border-color: $color-marine-blue;
  background-color: $color-marine-blue;

  &:hover {
    border-color: $color-marine-blue-transparent;
    background-color: $color-marine-blue-transparent;
  }
  & .title {
    color: $color-white;
  }

  & .arrow {
    background-color: $color-white;
  }
}

.primary--2 {
  border-color: $color-yellow;
  background-color: $color-yellow;

  &:hover {
    border-color: $color-yellow-light;
    background-color: $color-yellow-light;
  }
  & .title {
    color: $color-black;
  }

  & .arrow {
    background-color: $color-black;
  }
}

.secondary--1 {
  border-color: $color-marine-blue;
  background-color: $bg-main-color;

  &:hover {
    border-color: $color-marine-blue;
    background-color: $color-marine-blue;

    & .title {
      color: $color-white;
    }

    & .arrow {
      background-color: $color-white;
    }
  }
  & .title {
    color: $color-black;
  }

  & .arrow {
    background-color: $color-black;
  }
}

.secondary--2 {
  border-color: $color-dark-grey;
  background-color: $bg-main-color;

  &:hover {
    background-color: $color-white;
  }
  & .title {
    color: $color-dark-grey;
  }

  & .arrow {
    background-color: $color-dark-grey;
  }
}
</style>
