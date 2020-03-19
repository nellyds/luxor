<template>
  <v-app>
  <NavBar />
  <v-container class="topSpace" />

<router-view></router-view>
<Lower />
        <v-footer app
        color=black
        >
              <v-divider></v-divider>
          <v-card-text>
      <span class="footerText"><a href="http://www.nelson-dsilva.com" >Nelson D'Silva &copy; 2020</a></span>
          </v-card-text>
    </v-footer>
  </v-app>
</template>

<script>
import Lower from "@/components/Lower";
import NavBar from "@/components/NavBar.vue";
export default {
  name: "App",
  components: {
    Lower,
    NavBar
  },
  data: () => ({
    //
  })
};
</script>
<style scoped>
.topSpace{
padding-top: 10px;
  height: 2em;

}
.linkText{
  color: black;
  text-decoration: none;
  padding: 1em;
  font-size: 1.2em;
}
a{
  text-decoration: none;

  
}
a:visited{
  text-decoration: none;

}
.footerText{
 
   text-decoration-color: white;

  color: white;
  text-decoration: none;





}
.lowerDivide{
  min-width: 100%;
  min-height: 100px;
  background-color: black;
}
</style>
