<template>
  <div class="articleComponent">
    <img :src="img" alt="" />
    <small>{{ small }}</small>
    <h3>{{ title }}</h3>
    <p>
      {{ content }}
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "articleCard",

  props: {

    img: String,
    small: String,
    title: String,
    content: String,
  },
});
</script>

<style lang="scss" scoped>
$secundary-color: hsl(233, 26%, 24%);
$forth-color: hsl(0, 0%, 100%);
$fifth-color: hsl(233, 8%, 62%);
$breakpoint-laptop: 1070px;

.articleComponent {
  width: 80%;
  height: 60%;
  line-height: 1.6;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  border-radius: 8px;
  margin: auto;
  margin-top: 40px;
  background-color: white;
  box-shadow: 5px 5px 10px grey;
  padding: 10px 0px 20px;

  & h3{
    padding: 5px;
  }
  & img {
    width: 90%;
    height: 50%;
  }
}

@media (min-width: $breakpoint-laptop) {
  .articleComponent {
    width: 30%;
    height: 50%;

    & img{
        width: 100%;
    }
  }
}
</style>
