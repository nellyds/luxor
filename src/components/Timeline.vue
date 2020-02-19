<template>
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
</template>

<script>
export default {
  name: "Timeline",
  data(){
      return{
        processSteps: [
        {description : "Schedule a no-cost analysis where one of our efficiency experts will audit your facility and explain the different lighting options available to you"},
        {description:"Luxor Energy Solutions will develop a proposal delineating the ROI, 10-year cash flows, and environmental impact of the efficiency upgrade"},
        {description:"Upon contract execution, financing will be arranged(if applicable) and the rebate applications will be submitted "},
        {description:"Luxor Energy Solutions will conduct a pre-installation walk through with one of our trusted electrical contractors(if desired) or with the installer of your choice"},
        {description:"Once the rebate is pre-approved, all materials are ordered and delivered from one of our local warehouses"},
        {description:"Installation is completed"},
        {description:"Once we confirm you are thoroughly satisfied with your new lighting, we will submit the final rebate documents to the appropriate authorities"},
        {description:"Rebate checks arrive in 4-6 weeks"}
      ]
      }
  }
}

</script>
