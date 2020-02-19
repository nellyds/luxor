<template>
  <div class="about">
    
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
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>
    </v-img>
  </v-card>
  </div>
</template>
<script>
export default {
  name: 'about',
  data(){
    return {
      aboutContent:[
        {name: "James D'Silva", role: "CEO"},
        {name: "Karan Singh", role:"CEO"},
        {name: "Malcolm D'Silva", role:"CEO"},
        {name: "Race Carino", role:"CEO"}
      ]
    }
  }
}
</script>
