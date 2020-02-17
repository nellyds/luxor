<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <iframe width="560" height="315" src="https://www.youtube.com/embed/zPBb2W9GQAg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
  
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  }
};
</script>
