<template>
  <div class="Lower">
   
     <v-bottom-navigation
    v-model="bottomNav"
    dark
    shift
  >
    <v-btn>
<i style="font-size:24px;color:rgb(100,100,200)" class="fa">&#xf08c;</i>
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
    min-height: 400px;
}
</style>