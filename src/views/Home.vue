<template>
  <div class="home">
     <v-container >
       <div class="center">
  <v-jumbotron color="grey lighten-2">
    <v-container fill-height>
      <v-layout align-center>
        <v-flex>
              <v-row
      align="center"
      justify="center"
    >
          <v-img src="@/assets/LUXOR.jpg" :max-width=400 :aspect-ratio="16/16"/>
              </v-row>
                    <v-divider class="my-3"></v-divider>
        </v-flex>
      </v-layout>
    </v-container>
  </v-jumbotron>
<v-parallax
    dark
    src="https://i.imgur.com/M2Q4rh9.jpg"
  >
    <v-row
      align="center"
      justify="center"
    >
    </v-row>
  </v-parallax>
  <v-divider class="my-3"></v-divider>
   <v-flex text-xs-center>
                        <v-row
                        :align="align"

      justify="center"
    >
  <Info image="https://i.imgur.com/bhLZXMr.jpg" v-bind:content=intro_copy />
  <Info image="https://i.imgur.com/Ecs9eZU.jpg" v-bind:content=middle_copy />
   <Info image='https://i.imgur.com/E7dBP6K.jpg' v-bind:content=close_copy> </Info>
                        </v-row>
   </v-flex>
   <v-jumbotron color="primary" dark>
    <v-container fill-height>
      <v-layout align-center>
        <v-flex text-xs-center>
                        <v-row
      align="center"
      justify="center"
    >
          <h3 class="display-3">What We Do For You</h3>
                        </v-row>
                        <v-divider class="my-3"></v-divider>
        </v-flex>
      </v-layout>
    </v-container>
  </v-jumbotron>

<Timeline />
  <Case />
       </div>
  </v-container>
  </div>
  
</template>

<script>
import Case from "@/components/Case";
import Timeline from "@/components/Timeline";
import Info from "@/components/Info";
export default {
  name: "Home",
  components: {
    Timeline,
    Case,
    Info
  },
  data(){
    return {
      slogan:"Upgrade to LED today and save 50-75% on your electric bill while improving the aesthetics and safety of your facility",
      intro_copy:"Luxor Energy Solutions specializes in helping facilities reduce their energy costs through lighting retrofits while dramatically improving light levels, safety, and employee morale. ",
      close_copy:"95% if our products come from American owned companies. All of our products are designed to last for at least 10 years, and are guaranteed for at least 5",
      middle_copy: "Our unique process leverages utility rebates and federal programs to provide our clients with unparalleled ROIs for their efficiency projects. The vast majority see returns under two years, many well one year, and some are able to upgrade their lighting with absolutely no out of pocket expense at all!",
    fixtures: ["400 W Metal Halide","250 W Metal Halide", "2x4 Troffer",  "2x2 Troffer", "6-Lamp T5 High Bay",  "4-Lamp T5 High Bay", "6-Lamp T8 High Bay"],
    reductions: [61,72,63,53,59,55,48]


        
    
    }
  }
};
</script>
<style>
body{
  margin: auto;
}
.timeLine{

}
.introDiv{

  background-image: url("https://i.imgur.com/M2Q4rh9.jpg");
  
  
}
</style>

