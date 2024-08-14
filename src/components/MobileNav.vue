<template>
  <nav class="navbar">
    <div class="logo">
        <img src="../assets/images/Logo.svg" alt="logo" />
        <p>Berry</p>
    </div>
    <div class="menu-icon" @click="toggleMenu">
      <img v-if="!menuOpen" src="../assets/images/hamburger.svg" alt="Hamburger Icon" />
      <img v-if="menuOpen" src="../assets/images/cancel.svg" alt="Cancel Icon" />
    </div>
    <ul :class="{ 'nav-items': true, open: menuOpen }">
      <li>
        <img src="../assets/images/Housenav.svg" alt="Homelogo">
        <router-link to="/">Home</router-link>
      </li>
      <li>
        <img src="../assets/images/UsersThreemob.svg" alt="">
        <router-link to="/about">About</router-link>
      </li>
    </ul>
  </nav>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MobileNav",
  setup() {
    const menuOpen = ref(false);

    const toggleMenu = () => {
      menuOpen.value = !menuOpen.value;
    };

    return {
      menuOpen,
      toggleMenu,
    };
  },
});
</script>
<style scoped>
@import "../components/mobileNav.css";
</style>
