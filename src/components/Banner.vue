<template>
  <section class="banner">
    <div
      data-aos="fade-right"
      data-aos-offset="300"
      data-aos-easing="ease-in-sine"
      data-aos-duration="1000"

      class="wallpaper"
    >
      <img src="../assets/image-mockups.png" alt="phone images" />
    </div>
    <div class="requestArea">
      <h1
        data-aos="fade-down"
        data-aos-easing="linear"
        data-aos-duration="1500"
      >
        Next generation digital banking
      </h1>
      <p>
        Take your financial life online. Your Easybank account will be a
        one-stop-shop for spending, saving, budgeting, investing, and much more.
      </p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "bannerPg",
});
</script>

<style lang="scss" scoped>
$title-color: hsl(233, 26%, 24%);
$breakpoint-laptop: 1071px;

.banner {
  width: 100%;
  height: 100%;
  & .wallpaper {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;

    background-image: url(../assets/bg-intro-mobile.svg);
    background-repeat: no-repeat;
    background-size: contain;
    background-position-x: right;

    & svg {
      width: 100%;
    }

    & img {
      max-width: 100%;
      left: 0;
    }
  }

  .requestArea {
    width: 80%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: auto;
    text-align: center;
    line-height: 2;

    & h1 {
      font-size: 2rem;
      color: $title-color;
      padding: 10px;
    }
  }
}

@media (min-width: $breakpoint-laptop) {
  .banner {
    width: 100%;
    height: 100%;
    margin: auto;

    & .wallpaper {
      position: relative;
      width: 100%;
      height: 80vh;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: space-around;
      background-size: 100%;
      background-position-x: right;
      overflow: hidden;

      & img {
        max-width: 30rem;
      }
    }
    & .requestArea {
      & h1 {
        font-size: 5rem;
      }
      & p {
        font-size: 1.5rem;
      }
    }
  }
}
</style>
