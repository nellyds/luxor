<template>
  <v-app>
      <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'white' : 'rgba(255, 255, 255, 0)'"
    :hide-on-scroll="$vuetify.breakpoint.smAndDown"
    app
  
    elevate-on-scroll
  >
   <v-row
      align="center"
      justify="center"
    >
 
    <v-img
      class="shrink"
      max-width="1em"
      src="@/assets/LUXORby-01.jpg" 
    />
    <router-link class="linkText" to="/">Home</router-link>
    <router-link class="linkText" to="/about">About Us</router-link>
    <router-link class="linkText" to="/services">Our Services</router-link>
    <router-link class="linkText" to="/contact">Contact</router-link>

   </v-row>

  </v-app-bar>
<router-view></router-view>
<Lower />
        <v-footer app
        color=white
        >
              <v-divider></v-divider>
          <v-card-text>
      <span class="footerText">Nelson D'Silva &copy; 2020</span>
          </v-card-text>
    </v-footer>
  </v-app>
</template>

<script>
import Lower from "@/components/Lower"
export default {
  name: "App",
  components: {
    Lower
  },
  data: () => ({
    //
  })
};
</script>
<style scoped>
.linkText{
  color: black;
  text-decoration: none;
}
.lowerDivide{
  min-width: 100%;
  min-height: 100px;
  background-color: black;
}
</style>
