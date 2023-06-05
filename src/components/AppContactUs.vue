<template>
  <div class="contactUs">
    <div class="contactUs__formBlock">
      <div class="contactUs__titles">
        <div class="contactUs__title">have any questions?</div>
        <div class="contactUs__subtitle">
          Here few ways to get in touch with us:
        </div>
      </div>
      <form class="contactUs__form">
        <div class="contactUs__formTitle">Message us</div>
        <div class="contactUs__formInputs">
          <AppInput type="text" placeholder="Name" />
          <AppInput type="email" placeholder="Email" />
          <AppInput type="text" placeholder="Message" />
        </div>
        <AppButton
          type="button"
          :handleClick="handleTestClick"
          className="primary--1"
          buttonTitle="Submit"
        ></AppButton>
      </form>
    </div>
    <!-- <div class="contactUs__contacts">Contact Us</div> -->
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import AppButton from "../ui/AppButton.vue";
import AppInput from "@/ui/AppInput.vue";

export default defineComponent({
  components: {
    AppButton,
    AppInput,
  },
  setup() {
    const handleTestClick = () => console.log("click");

    return {
      handleTestClick,
    };
  },
});
</script>

<style lang="scss" scoped>
@import "../styles/main.scss";
.contactUs {
  margin-top: 80px;
  padding-top: 70px;
  display: flex;
  justify-content: space-between;

  &__formBlock {
    display: flex;
    flex-direction: column;
    gap: 30px;
    flex-basis: 33.3%;
  }

  &__titles {
    display: flex;
    flex-direction: column;
  }

  &__title {
    font-family: "Bebas Neue";
    font-style: normal;
    font-weight: 400;
    font-size: 36px;
    line-height: 150%;
    letter-spacing: 0.155em;
  }

  &__subtitle {
    font-family: "Manrope";
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 150%;
  }

  &__form {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }

  &__formTitle {
    font-family: "Manrope";
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 150%;
  }

  &__formInputs {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
}
</style>
