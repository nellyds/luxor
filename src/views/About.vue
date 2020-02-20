<template>
  <div class="about">
     <v-row
      align="center"
      justify="center"
    >
    <Profile v-bind:image="image" />
        <Profile v-bind:image="image" />
            <Profile v-bind:image="image" />
    
    </v-row>
    <v-card
     v-for="about in aboutContent"
      :key="about"
    class="mx-auto"
    max-width="434"
    tile
  >
    <v-img
      height="100%"
      src="@/assets/bulbs.jpg"
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
          <v-avatar
            class="profile"
            color="grey"
            size="164"
            tile
          >
           
          </v-avatar>
        </v-col>
        <v-col class="py-0">
          <v-list-item
            color="rgba(0, 0, 0, .4)"
            dark
          >
            <v-list-item-content>
              <v-list-item-title class="title">{{about.name}}</v-list-item-title>
              <v-list-item-subtitle>{{about.role}}</v-list-item-subtitle>
              <v-list-item-title class="title">{{about.E}}</v-list-item-title>
              <v-list-item-title class="title">{{about.M}}</v-list-item-title>
              <v-list-item-title class="title">{{about.linkedin}}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>
    </v-img>
  </v-card>
  </div>
</template>
<script>
import Profile from "@/components/Profile"
export default {
  name: 'about',
  components:{
    Profile
  },
  data(){
    return {
      aboutContent:[
        {name: "Malcolm D'Silva", role: "President & CEO", M:"(440)759-8911",E: "james@luxorenergysolutions.com", linkedin:"https://www.linkedin.com/in/mjdsilva/", bio:""},
        {name: "Karan Singh", role:"National Accounts Manager", M:"(937)902-5715", E:"karan@luxorenergysolutions.com", linkedin:"", bio:""},
        {name: "James D'Silva MD", role:"Chief Operations Officer", M:"(440)539-5492",E:"james@luxorenergysolutions.com", linkedin:"https://www.linkedin.com/in/james-dsilva-a44ba97a/", bio:""},
        {name: "Race Carino", role:"Vice President of Sales, NorthEast", M: "M: (775)842-8573", E: "race@luxorenergysolutions.com", linkedin: "https://www.linkedin.com/in/race-carrino-b26a27110/", bio:""}
      ],
      image: "https://previews.123rf.com/images/maxoidos/maxoidos1312/maxoidos131200228/24209298-interior-of-new-large-and-modern-warehouse-space.jpg"
    }
  }
}
</script>
