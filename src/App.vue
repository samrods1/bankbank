<template>
  <main>
    <nav class="navContent">
      <nav-bar />
      <banner />
      <form1/>
    </nav>
    <section class="contentWrapper">
      <why-easybank />
    </section>
    <section>
     <articles/> 
    </section>
    <footer>
      <footer1/>
    </footer>
  </main>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "./components/NavBar.vue";
import Banner from "./components/Banner.vue";
import WhyEasybank from "./components/WhyEasybank.vue";
import Articles from "./components/Articles.vue";
import Footer1 from "./components/Footer.vue";
import Form1 from "./components/Form.vue";
export default defineComponent({
  name: "App",
  components: {
    NavBar,
    Banner,
    WhyEasybank,
    Articles,
    Footer1,
    Form1
},
});
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Playfair+Display:ital@0;1&family=Staatliches&display=swap");

* {
  text-decoration: none;
  list-style-type: none;
  margin: 0;
  font-family: "Staatliches";
  overflow-x: hidden;
}

:root {
  $primary-color: hsl(136, 65%, 51%);
  $secundary-color: hsl(233, 26%, 24%);
  $terceary-color: hsl(192, 70%, 51%);
  $forth-color: hsl(0, 0%, 100%);
  $fifth-color: hsl(233, 8%, 62%);
}
p,
h3 {
  font-family: "Playfair";
}
</style>
