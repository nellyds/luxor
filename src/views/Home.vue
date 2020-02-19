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
                                  <v-row
      align="center"
      justify="center"
    >
          <span class="subheading">{{intro_copy}}</span>
                                  </v-row>

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
<v-container class="timeLine">
  <v-timeline>
    <v-timeline-item
      v-for="step in processSteps"
      :key="step"
      color="yellow lighten-2"
      large
      fill-dot
    >
                
              <v-hover
                    v-slot:default="{ hover }"
                    open-delay="200"
                  >
                    <v-card
                      :elevation="hover ? 16 : 2"
                      >
                    <v-card-text>
                      {{step.description}}
                    </v-card-text>
                  </v-card>
                </v-hover>
                </v-timeline-item>
              </v-timeline>
              </v-container>
    <v-card
      class="mt-4 mx-auto"
      max-width="400"
    >
  <v-sheet
        class="v-sheet--offset mx-auto"
        color="yellow"
        elevation="12"
        max-width="calc(100% - 32px)"
      >
        <v-sparkline
          :labels="fixtures"
          :value="reductions"
          
          color="white"
          line-width="2"
          padding="45"
        ></v-sparkline>
      </v-sheet>
        <v-card-text class="pt-0">
        <div class="title font-weight-light mb-2">Average Percentage Reduction in Wattage</div>

        <span class="caption grey--text font-weight-light">last registration 26 minutes ago</span>
      </v-card-text>
    </v-card>
     <v-card
      class="mt-4 mx-auto"
      max-width="400"
    >
    <v-card-text>{{close_copy}} </v-card-text>
     </v-card>
       </div>
  </v-container>
  </div>
  
</template>

<script>

export default {
  name: "Home",
  components: {
  },
  data(){
    return {
      slogan:"Upgrade to LED today and save 50-75% on your electric bill while improving the aesthetics and safety of your facility",
      intro_copy:"Luxor Energy Solutions specializes in helping facilities reduce their energy costs through lighting retrofits while dramatically improving light levels, safety, and employee morale. ",
      close_copy:"95% if our products come from American owned companies. All of our products are designed to last for at least 10 years, and are guaranteed for at least 5",
      processSteps: [
        {description : "Schedule a no-cost analysis where one of our efficiency experts will audit your facility and explain the different lighting options available to you"},
        {description:"Luxor Energy Solutions will develop a proposal delineating the ROI, 10-year cash flows, and environmental impact of the efficiency upgrade"},
        {description:"Upon contract execution, financing will be arranged(if applicable) and the rebate applications will be submitted "},
        {description:"Luxor Energy Solutions will conduct a pre-installation walk through with one of our trusted electrical contractors(if desired) or with the installer of your choice"},
        {description:"Once the rebate is pre-approved, all materials are ordered and delivered from one of our local warehouses"},
        {description:"Installation is completed"},
        {description:"Once we confirm you are thoroughly satisfied with your new lighting, we will submit the final rebate documents to the appropriate authorities"},
        {description:"Rebate checks arrive in 4-6 weeks"}
      ],
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

