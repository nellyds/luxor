<template>
  <div class="about">
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
     <v-row
      align="center"
      justify="center"
    >
    </v-row>
    <v-card
     v-for="about in aboutContent"
      :key="about"
    class="mx-auto"
    max-width="434"
    tile
  >

      <v-row
        align="end"
        class="fill-height"
      >
        <v-col
          align-self="start"
          class="pa-0"
          cols="12"
        >
        </v-col>
        <v-col class="py-0">
          <v-list-item
            color="black"
            
          >
            <v-list-item-content>
              <v-list-item-title class="title">{{about.name}}</v-list-item-title>
              <v-list-item-subtitle>{{about.role}}</v-list-item-subtitle>
              <v-list-item-title class="title">{{about.E}}</v-list-item-title>
              <v-list-item-title class="title">{{about.M}}</v-list-item-title>
              <a v-bind:href=about.linkedin ><i style="font-size:24px;color:rgb(0,0,0)" class="fa">&#xf08c;</i></a>
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>

  </v-card>
  </div>
</template>
<script>
export default {
  name: 'about',
  components:{

  },
  data(){
    return {
      aboutContent:[
        {name: "Malcolm D'Silva", role: "President & CEO", M:"(440)759-8911",E: "malcolm@luxorenergysolutions.com", linkedin:"https://www.linkedin.com/in/mjdsilva/", bio:""},
        {name: "Karan Singh", role:"National Accounts Manager", M:"(937)902-5715", E:"karan@luxorenergysolutions.com", linkedin:"", bio:""},
        {name: "James D'Silva MD", role:"Chief Operations Officer", M:"(440)539-5492",E:"james@luxorenergysolutions.com", linkedin:"https://www.linkedin.com/in/james-dsilva-a44ba97a/", bio:""},
        {name: "Race Carino", role:"Vice President of Sales, NorthEast", M: "M: (775)842-8573", E: "race@luxorenergysolutions.com", linkedin: "https://www.linkedin.com/in/race-carrino-b26a27110/", bio:""}
      ],
      image: "https://previews.123rf.com/images/maxoidos/maxoidos1312/maxoidos131200228/24209298-interior-of-new-large-and-modern-warehouse-space.jpg"
    }
  }
}
</script>
<style scoped>

</style>
