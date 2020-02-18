<template>
  <v-app>
      <!-- <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'rgba(66, 66, 66, .9)'"
    :hide-on-scroll="$vuetify.breakpoint.smAndDown"
    app
    dark
    elevate-on-scroll
  > -->
    <!-- <v-img
      alt="Alpha Construction"
      class="shrink"
      max-width="15%"
      height="auto"
      src="@/assets/LUXORby-01.jpg" 
    /> -->
    <!-- <router-link to="/">Home</router-link>
    <router-link to="/about">About Us</router-link>
    <router-link to="/services">Our Services</router-link>
    <router-link to="/contact">Contact</router-link> -->



  <!-- </v-app-bar> -->
<router-view></router-view>
  </v-app>
</template>

<script>

export default {
  name: "App",



  data: () => ({
    //
  })
};
</script>
