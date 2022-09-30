<template>
  <div class="whyContainer">
    <h2 data-aos="zoom-in-down">Why choose Easybank?</h2>
    <WhyComponent
      data-aos="flip-left"
      data-aos-easing="ease-out-cubic"
      data-aos-duration="2000"
      :img="whyItems[0].img"
      :title="whyItems[0].title"
      :description="whyItems[0].content"
    />
    <WhyComponent1
      data-aos="flip-right"
      data-aos-easing="ease-out-cubic"
      data-aos-duration="2000"
      :img="whyItems[1].img"
      :title="whyItems[1].title"
      :description="whyItems[1].content"
    />
    <WhyComponent2
      data-aos="flip-left"
      data-aos-easing="ease-out-cubic"
      data-aos-duration="2000"
      :img="whyItems[2].img"
      :title="whyItems[2].title"
      :description="whyItems[2].content"
    />
    <WhyComponent3
      data-aos="flip-right"
      data-aos-easing="ease-out-cubic"
      data-aos-duration="2000"
      :img="whyItems[3].img"
      :title="whyItems[3].title"
      :description="whyItems[3].content"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import WhyComponent from "./WhyComponent.vue";
import WhyComponent1 from "./WhyComponent.vue";
import WhyComponent2 from "./WhyComponent.vue";
import WhyComponent3 from "./WhyComponent.vue";
import WhyComponent4 from "./WhyComponent.vue";

export default defineComponent({
  name: "whyComponent",

  data() {
    return {
      whyItems: [
        {
          img: require('../assets/icon-online.svg'),
          title: " Online Banking",
          content:
            " Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.",
        },
        {
          img: require('../assets/icon-budgeting.svg'),
          title: "Simple Budgeting",
          content:
            " See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits.",
        },
        {
          img: require('../assets/icon-onboarding.svg'),
          title: " Fast Onboarding",
          content:
            "We don’t do branches. Open your account in minutes online and start taking control of your finances right away.",
        },
        {
          img: require('../assets/icon-api.svg'),
          title: "Open API",
          content:
            "Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.",
        },
      ],
    };
  },
  components: {
    WhyComponent,
    WhyComponent1,
    WhyComponent2,
    WhyComponent3,
    WhyComponent4,
  },
});
</script>

<style lang="scss">
.whyContainer {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  margin: 10rem auto;
  text-align: center;
  background-color: hsl(233, 26%, 24%);

  & h2 {
    font-size: 3rem;
    padding: 2rem 0;
    color: hsl(0, 0%, 100%);
  }
}
</style>
