<template>
  <div class="whyComponents">
   <img :src="img" alt="images">
    <h3>{{title}}</h3>
    <p>
      {{description}}
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "whyComponent",

  props:{
    img: String,
    title: String,
    description: String
  }
  
});
</script>

<style lang="scss">
$breakpoint-laptop: 1070px;

.whyComponents {
  width: 80%;
  height: 20rem;
  margin-top: 3rem;
  margin-bottom: 3rem;
  line-height: 1.6;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  border-radius: 8px;
  background: #ffffff;

  & p {
    width: 80%;
  }
}

@media (min-width: $breakpoint-laptop) {
  .whyComponents {
    width: 50%;
  }
}
</style>
