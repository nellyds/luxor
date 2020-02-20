<template>
    <v-hover v-slot:default="{ hover }">
      <v-card
        class="mx-auto"
        color="grey lighten-4"
        max-width="600"
      >
        <v-img
          :aspect-ratio="9/9"
          :src="image"
        >
          <v-expand-transition>
            <div
              v-if="hover"
              class="d-flex transition-fast-in-fast-out black darken-2 v-card--reveal display-3 white--text"
              style="height: 100%;"
            >
              {{bio}}
            </div>
          </v-expand-transition>
        </v-img>
        <v-card-text
          class="pt-6"
          style="position: relative;"
        >
          <v-btn
            absolute
            color="orange"
            class="white--text"
            fab
            large
            right
            top
          >
            <v-icon><a href=linkedin class="fa fa-facebook"></a></v-icon>
          </v-btn>
          <div class="font-weight-light grey--text title mb-2">{{name}}</div>
          <h3 class="display-1 font-weight-light orange--text mb-2">{{role}}</h3>
          <v-divider />
          {{E}}
          {{M}}
        </v-card-text>
      </v-card>
    </v-hover>
</template>

<script>
export default {
    name: "Profile",
    props: {
    image: {
        type: String
    },
    name: {
        type: String
    },
    role: {
        type: String
    },
    E: {
        type: String
    },
    M: {
        type: String
    },
    linkedin: {
        type: String
    }
}
}
</script>
<style>
.v-card--reveal {
align-items: center;
bottom: 0;
justify-content: center;
opacity: .5;
position: absolute;
width: 100%;
}
</style>
