<template>
  <div class="home">
    <v-responsive>
    <div class="intro">
    <div class="overlayHolder d-none d-lg-block">
    <v-row>    
      <img data-aos="fade-up" data-aos-duration="1000" class=" logo" src="@/assets/overlaySquare.png" />
    </v-row>
    </div>
    <div class="overlayMobile d-lg-none">
        <img src="@/assets/luxorLogo.png" />
    </div>

    </div>
    </v-responsive>

    <v-parallax src="@/assets/bridge.jpg">
    <v-row class="valueRow">
      <v-col cols="12" sm="4">
    <div data-aos="fade-left" data-aos-duration="1500" class="valueContainer">
      {{values[0]}}
      </div>
      </v-col>
      <v-col cols="12" sm="4">
          <div data-aos="fade-up" data-aos-duration="1300" class="valueContainer">
      {{values[1]}}
      </div>
      </v-col>
      <v-col cols="12" sm="4">
          <div data-aos="fade-right" data-aos-duration="1500" class="valueContainer">
      {{values[2]}}
      </div>
      </v-col>
    </v-row>
    </v-parallax>
<Info />
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
  <v-parallax src="@/assets/pan.jpg">
  <div data-aos="fade-right" data-aos-duration="1500" class="closeHolder d-none d-lg-block">
    <p data-aos="fade-left" data-aos-duration="1500" class="closeCopy" >{{closeCopy}} </p>
    </div>

    <p data-aos="fade-left" data-aos-duration="1500" class="closeCopy d-lg-none" >{{closeCopy}} </p>

  </v-parallax>
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
      fixtures: ["400 W Metal Halide","250 W Metal Halide", "2x4 Troffer",  "2x2 Troffer", "6-Lamp T5 High Bay",  "4-Lamp T5 High Bay", "6-Lamp T8 High Bay"],
      reductions: [61,72,63,53,59,55,48],
      values:
    [
      'Manage your efficiency goals for LEDS lighting',
      'Receive Objective advice and access to over 150 vendors to source the most cost-effective solutions for your enterprise.',
      'Develop a custom buying strategy based on your needs.  Suppliers bid for your business.  You see the savings.'
    ],
    closeCopy:"Time is running out and the cost of energy is not going down soon. It's time to think about a more sustainable lighting solution. LED lighting offers superior visibility thanks to its white light and a safer technology with close to zero UV emission and no mercury. LED lighting is not only better for your eyes but also better for the environment."

    }
  },
  computed: {
    binding() {
      const binding = {}
      if (this.$vuetify.breakpoint.smAndDown) binding.column = true
      return binding
    }
  },

};
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Questrial&display=swap');
body{
  font-family: 'Questrial', sans-serif
}
.chartHolder{
  margin: auto;
  width: 600px;
}
.overlayHolder{
  height: 780px;
  background-size: 780px;
  background-image: url('https://i.imgur.com/b7EtWSO.jpg');
    background-attachment: fixed;
  background-position-x: center;
    margin-left: 33%;
}
.overlayMobile{
    background-image: url('https://i.imgur.com/b7EtWSO.jpg');
    background-attachment: fixed;
        background-attachment: fixed;
  background-position-y:initial;
  background-size: 375px;
}
.logo{
  height: auto;
  width: auto;
  object-fit: cover;
}
.valueContainer{
  border: solid white 3px;
  font-weight: bolder;
  color:white;
  align-content: center;
  padding: 10px;
  margin: auto;
 height: 10em;
 width: 15em;
 font-family: 'Questrial', sans-serif;
  max-width: 300px;
}
.valueRow{
  margin-top: 8%;
}
.closeCopy{
  color: white;
  font-size: 1.5em;
  padding: 10px;
  border: solid 3px white;
   font-family: 'Questrial', sans-serif;
   font-weight: bolder;
  }
  .closeHolder{
    max-width: 50%;
    margin: auto;
  }
  

</style>

