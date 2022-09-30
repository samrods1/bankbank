<template>
    <div
      class="container"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="48px"
        viewBox="0 0 24 24"
        width="72px"
        fill="#FFFFFF"
      >
        <path d="M0 0h24v24H0V0z" fill="none" />
        <path d="M9 16.2L4.8 12l-1.4 1.4L9 19 21 7l-1.4-1.4L9 16.2z" />
      </svg>
      <h3>{{ approved }}</h3>
    </div>
 
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "approved",

  data() {
    return {
      approved:
        "Your invite was successfully submited. Our staff will contact you very as soon as possible!",
    };
  },
});
</script>

<style lang="scss" scoped>
$primary-color: hsla(137, 98%, 51%, 0.986);
$breakpoint-tablet: 730px;
.container {
  position: absolute;
  top: 0;
  left: 0; 
  right: 0; 
  margin-left: auto; 
  margin-right: auto;
  z-index: 10;
  width: 100%;
  height: 100%;

  background: $primary-color;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  & svg {
    padding: 2rem 0;
    margin-bottom: 2rem;
    border-radius: 0px 50px;
    background-color: rgba(206, 206, 206, 0.267);
  }

  & h3 {
    width: 80%;
    font-size: 1.5rem;
    text-align: center;
  }
}

@media screen and (min-width: $breakpoint-tablet ) {
  .container{
    max-width: 100%;
    max-height: 100%;
  }
}
</style>
