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
  <Case class="chartHolder" />
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
      intro_copy:"Luxor Energy Solutions is a consulting and energy services firm that specializes in helping commercial, multifamily, and industrial buildings drastically reduce their energy cost and consumption.  Through lighting retrofits and efficiency audits we employ the latest innovative cutting edge technologies to dramatically improve light levels, safety, and environment all while helping your business become a leader in the Green economy.  The world is changing and new demands from government, the environment, and clients makes competing in the current business climate fraught with challenges....Luxor energy solutions shines the light so that you can lead the way.  We get big jobs done right.",
      close_copy:"We pride ourselves on the products we deliver with over 95% coming from American owned companies.  While our aesthetic sensibilities are a significant asset, we demand durability along with quality, and our products are designed to last for at least a decade with a minimum of a 5 year guarantee.",
      middle_copy: "Our unique process allows us to leverage utility rebates as well as federal and state programs in combination with a deep understanding of energy market and opportunities to provide clients with a customized energy efficiency upgrade with truly unparalleled return on investment.  The savings your business will accrue will be evident from the from the first utility bill after our upgrade and continue year after year.  These substantial savings that coincide with your lighting upgrade are often done with no out of pocket expense at all.",
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
.chartHolder{
  margin: auto;
  width: 600px;
}
.timeLine{
}
.introDiv{
  background-image: url("https://i.imgur.com/M2Q4rh9.jpg");
}
</style>

