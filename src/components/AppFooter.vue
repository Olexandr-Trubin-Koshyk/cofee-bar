<template>
  <div class="footer">
    <div class="contentWrapper">
      <div class="footer__mainBlock">
        <div class="footer__addressBlock">
          <div class="footer__title">Address</div>
          <div class="footer__subTitle" @click="goToSocialPage(links.map)">
            United Kingdom 99 Staple Hill Road, Bristol, BS16 5AD
          </div>
        </div>
        <div class="footer__socialsBlock">
          <div class="footer__socials">
            <div
              class="footer__socialIcon footer__socialIcon--twitter"
              @click="goToSocialPage(links.twitter)"
            ></div>
            <div
              class="footer__socialIcon footer__socialIcon--instagram"
              @click="goToSocialPage(links.instagram)"
            ></div>
            <div
              class="footer__socialIcon footer__socialIcon--facebook"
              @click="goToSocialPage(links.facebook)"
            ></div>
          </div>
          <div class="footer__logo"><a href="#main">CoffeeBar</a></div>
        </div>
        <div class="footer__copywriteBlock">
          <div class="footer__title">About us</div>
          <div class="footer__subTitle">
            ©
            {{
              new Date().getFullYear() === 2023
                ? new Date().getFullYear()
                : "2023 - " + new Date().getFullYear()
            }}
            by CoffeeBar
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: {
        twitter: "https://twitter.com",
        instagram: "https://www.instagram.com",
        facebook: "https://facebook.com/",
        map: "https://goo.gl/maps/HC71kbtbdzdTZuSH7?coh=178571&entry=tt",
      },
    };
  },
  methods: {
    goToSocialPage(page) {
      window.open(page, "_blank");
    },
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
  align-items: center;
  justify-content: center;

  &__mainBlock {
    display: flex;
    justify-content: space-between;
    padding-top: 74px;
    padding-bottom: 64px;
  }

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
