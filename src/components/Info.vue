  <template>
  <div>
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src=image
    >
      
    </v-img>
    <v-card-text class="text--primary">

      <div>{{content}}</div>
    </v-card-text>
  </v-card>
    </div>
  
</template>

<script>
export default {

  name: "Info",
  components: {
  },
    props: {
    image: {
        type: String
    },
    content: {
        type: String
    }
}
};
</script>