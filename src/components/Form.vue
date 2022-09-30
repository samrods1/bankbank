<template>
  <section>
    <form ref="inputValue" @submit="notify" class="form">
      <label for="#name">Insert Your Name:</label>
      <input id="name" required type="text" />
      <label for="#surname">Insert Your Surname:</label>
      <input id="surname" required type="text" />
      <label for="#email">Insert Your email:</label>
      <input id="email" required type="email" />
      <label for="#tel">Insert Your Phone Number:</label>
      <input id="tel" required type="tel" placeholder="ex: 123-456-789" maxlength="9" pattern="[0-9]{3}[0-9]{3}[0-9]{3}"/>
      <BtnComponent />
      <Transition>
        <Approved v-if="isApproved" />
      </Transition>
    </form>
  </section>
</template>

<script lang="ts">
import { defineComponent, h } from "@vue/runtime-core";
import BtnComponent from "./BtnComponent.vue";
import Approved from "./Approved.vue";

export default defineComponent({
  name: "formComponent",
  components: { BtnComponent, Approved },
  data() {
    return {
      isApproved: false,
    };
  },

  methods: {
    notify(event: any) {
      event.preventDefault();
      this.isApproved = !this.isApproved;
      event.target.reset();
    },
  },
});
</script>

<style lang="scss">
$title-color: hsl(233, 26%, 24%);
form {
  position: relative;
  margin: auto auto;
  width: 80%;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 0px;
  background: $title-color;
  padding: 20px 0px;

  & label {
    width: 80%;
    text-align: left;
    color: #ffffff;
  }

  & input {
    width: 80%;
    margin: auto;
    padding: 10px;
  }
}

.v-enter-active,
.v-leave-active {
  transition: all 1s ease-in;
  transform: translateX(0px);
}

.v-enter-from,
.v-leave-to {
  transform: translateX(-1200px);
}

</style>
