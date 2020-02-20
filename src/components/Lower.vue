<template>
  <div class="Lower">
   
     <v-bottom-navigation
    v-model="bottomNav"
    background-color="black"
    shift
  >
    <v-btn>
<i style="font-size:24px;color:rgb(255,255,255)" class="fa">&#xf08c;</i>
    </v-btn>


  </v-bottom-navigation>
  </div>
  
</template>

<script>
// @ is an alias to /src

export default {
  name: "Lower",

};
</script>
<style scoped>
.Lower{
    min-height: 150px;
    background-color:black;
}
</style>