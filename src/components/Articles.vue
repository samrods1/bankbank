<template>
  <section>
    <h2 data-aos="zoom-in"
    data-aos-duration="1000"
    >Latest Articles</h2>
    <ArticleCard
      data-aos="fade-right"
      data-aos-anchor="#example-anchor"
      data-aos-offset="500"
      data-aos-duration="2000"
      :img="articleItems[0].img"
      :small="articleItems[0].small"
      :title="articleItems[0].title"
      :content="articleItems[0].content"
    />
    <ArticleCard
      data-aos="fade-left"
      data-aos-anchor="#example-anchor"
      data-aos-offset="500"
      data-aos-duration="3000"
      :img="articleItems[1].img"
      :small="articleItems[1].small"
      :title="articleItems[1].title"
      :content="articleItems[1].content"
    />
    <ArticleCard
      data-aos="fade-right"
      data-aos-anchor="#example-anchor"
      data-aos-offset="500"
      data-aos-duration="4000"
      :img="articleItems[2].img"
      :small="articleItems[2].small"
      :title="articleItems[2].title"
      :content="articleItems[2].content"
    />
    <ArticleCard
      data-aos="fade-right"
      data-aos-anchor="#example-anchor"
      data-aos-offset="500"
      data-aos-duration="5000"
      :img="articleItems[3].img"
      :small="articleItems[3].small"
      :title="articleItems[3].title"
      :content="articleItems[3].content"
    />
  </section>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import ArticleCard from "./ArticleCard.vue";

export default defineComponent({
  name: "articleComponent",
  components: { ArticleCard },
  data() {
    return {
      articleItems: [
        {
          img: require('../assets/image-currency.jpg'),
          small: "By Clair Robinson",
          title: "Receive money in any currency with no fees",
          content:
            "The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …",
        },
        {
          img: require('../assets/image-restaurant.jpg'),
          small: " By Wilson Hutton",
          title: " Treat yourself without worrying about money",
          content:
            "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …",
        },
        {
          img: require('../assets/image-plane.jpg'),
          small: "By Jay Kyle",
          title:
            "We want you to enjoy your travels. This is why we don’t charge any fees on purchases",
          content:
            "We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …",
        },
        {
          img: require('../assets/image-confetti.jpg'),
          small: "By Lora Moroe",
          title:
            "After a lot of hard work by the whole team, we’re excited to launch our closed beta.",
          content: "  It’s easy to request an invite through the site ...",
        },
      ],
    };
  },
});
</script>

<style lang="scss" scoped>
   $primary-color: hsl(136, 65%, 51%);
$secundary-color: hsl(233, 26%, 24%);
$forth-color: hsl(0, 0%, 100%);
$fifth-color: hsl(233, 8%, 62%);

section {
  width: 100%;
  height: 100%;
  background-color: hsl(0, 0%, 100%);
  display: flex;
  flex-direction: column;
  align-items: center;

  & h2 {
    font-size: 3rem;
    text-align: center;
    padding: 20px;
    color: $fifth-color;
  }
}
</style>
