<template>
  <button>Request Invite</button>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "btnComponent",

 
  
}); 
</script>

<style lang="scss">
$btn-color-1: hsl(136, 65%, 51%);
$btn-color-2: hsl(192, 70%, 51%);
$btn-font: hsl(0, 0%, 100%);
$title-color: hsl(233, 26%, 24%);
button {
  margin-top: 1rem;
  font-size: 1.2rem;
  padding: 20px 50px;
  border-radius: 2rem;
  border: 0;
  background: linear-gradient(to left, $btn-color-1 0%, $btn-color-2 100%);
  color: $btn-font;
}
button:hover {
  cursor: pointer;
  background: linear-gradient(to left, $btn-color-2 0%, $title-color 100%);
}
</style>
