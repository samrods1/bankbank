<template>
  <div class="footer">
    <img src="../assets/logo.svg" alt="logo" />
    <div class="mediaWrapper">
      <div class="media">
        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg"
        />

        <img
          src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"
        />
      </div>
      <div class="toggleMenu">
        <ul>
          <li v-for="item in menuItems" :key="item.key">
            <a href="#">{{ item.item }}</a>
          </li>
        </ul>
      </div>s
      <small>
        Challenge by Frontend Mentor. Coded by
        <a href="https://www.linkedin.com/in/samuelrods/" target="_blank"
          >Samuel Rodrigues</a
        >
        </small
      >
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";
import NavBar from "./NavBar.vue";

export default defineComponent({
  components: { NavBar },

  data() {
    return {
      menuItems: [
        { item: "Home", key: "0001" },
        { item: "About", key: "0002" },
        { item: " Contact", key: "0003" },
        { item: "Blog", key: "0004" },
        { item: "Careers", key: "0005" },
      ],
    };
  },
});
</script>

<style lang="scss">
$primary-color: hsl(136, 65%, 51%);
$secundary-color: hsl(233, 26%, 24%);
$terceary-color: hsl(139, 42%, 34%);
$forth-color: hsl(0, 0%, 100%);
$fifth-color: hsl(233, 8%, 62%);
footer {
  width: 100%;
  height: 100%;
  margin-top: 2rem;
  display: block;
  background-color: $terceary-color;
  padding: 30px 0;
  text-align: center;

  & .mediaWrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    & .media {
      width: 100%;
      padding: 20px;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: space-around;

      & img {
        width: 2rem;
      }
      img:hover {
        cursor: pointer;
      }
    }

    .toggleMenu {
      width: 100%;
      margin: auto;

      & li {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 20px;

        & a {
          color: $forth-color;
        }

        & a:hover {
          color: $secundary-color;
        }
      }

      & small {
        color: $primary-color;
      }
    }
    a {
      color: $forth-color;
    }
  }
}
</style>
