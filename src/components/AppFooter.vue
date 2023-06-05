<template>
  <div class="footer">
    <div
      class="footer__addressBlock"
      @click="openLink(contacts.map)"
      title="Click to see our location on Google Maps"
    >
      <div class="footer__title">Address</div>
      <div class="footer__subTitle">{{ contacts.address }}</div>
    </div>
    <div class="footer__socialsBlock">
      <div class="footer__socials">
        <div
          class="footer__socialIcon footer__socialIcon--twitter"
          @click="openLink(contacts.twitter)"
          title="Follow us on Twitter"
        ></div>
        <div
          class="footer__socialIcon footer__socialIcon--instagram"
          @click="openLink(contacts.instagram)"
          title="Follow us on Instagram"
        ></div>
        <div
          class="footer__socialIcon footer__socialIcon--facebook"
          @click="openLink(contacts.facebook)"
          title="Follow us on Facebook"
        ></div>
      </div>
      <div class="footer__logo">
        <a href="#main" title="To start of page">{{ siteTitle }}</a>
      </div>
    </div>
    <div class="footer__copywriteBlock">
      <div class="footer__title"><a href="#about-us">About us</a></div>
      <div class="footer__subTitle">
        ©
        {{ getCopywritesYears }}
        by {{ siteTitle }}
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import ContactsData from "@/types/ContactsData";
import { inject } from "vue";
import { computed } from "vue";
import { ref } from "vue";

export default {
  setup() {
    const siteTitle = inject("siteTitle");

    const contacts = ref<ContactsData>({
      twitter: "https://twitter.com",
      instagram: "https://www.instagram.com",
      facebook: "https://facebook.com/",
      map: "https://goo.gl/maps/HC71kbtbdzdTZuSH7?coh=178571&entry=tt",
      address: "United Kingdom 99 Staple Hill Road, Bristol, BS16 5AD",
    });

    const openLink = (page: string) => {
      page.startsWith("https://") && window.open(page, "_blank");
    };

    const getCopywritesYears = computed(() =>
      new Date().getFullYear() === 2023
        ? new Date().getFullYear()
        : "2023 - " + new Date().getFullYear()
    );

    return {
      contacts,
      openLink,
      getCopywritesYears,
      siteTitle,
    };
  },
};
</script>

<style lang="scss">
@import "../styles/main.scss";

.footer {
  position: relative;
  left: 0;
  bottom: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding-top: 74px;
  padding-bottom: 64px;

  &__addressBlock,
  &__copywriteBlock,
  &__socialsBlock {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  &__addressBlock,
  &__copywriteBlock {
    width: 170px;
  }

  &__addressBlock {
    cursor: pointer;
  }

  &__socialsBlock {
    justify-content: space-between;
    gap: 74px;
    width: 230px;
    text-align: center;
  }

  &__copywriteBlock {
    text-align: end;
  }

  &__title {
    font-family: "Bebas Neue";
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
  }

  &__socials {
    display: flex;
    justify-content: space-between;
  }

  &__socialIcon {
    background-repeat: no-repeat;
    background-size: cover;
    width: 30px;
    height: 30px;

    cursor: pointer;

    &--twitter {
      background-image: url(../assets/twitter-icon.svg);
    }

    &--instagram {
      background-image: url(../assets/instagram-icon.svg);
    }

    &--facebook {
      background-image: url(../assets/facebook-icon.svg);
    }
  }

  &__logo {
    font-family: "Bebas Neue";
    font-style: normal;
    font-weight: 400;
    font-size: 36px;
    line-height: 150%;

    letter-spacing: 0.155em;
    text-transform: uppercase;

    cursor: pointer;
  }
}
</style>
