  <template>
  <div>
  
     <v-row>
         <div v-for="copyItem in copy" :key="copyItem.text">
      <v-rol cols="16" sm="4">
      <div data-aos="fade-up" data-aos-duration="1000" class="holder">{{copyItem.text}}</div>
            </v-rol>
         </div>
     </v-row>

    </div>
  
</template>

<script>
export default {
  name: "Info",
  data(){
    return{
            copy:[
              {text:"Luxor Energy Solutions is a consulting and energy services firm that specializes in helping commercial, multifamily, and industrial buildings drastically reduce their energy cost and consumption."},
       {text: "Through lighting retrofits and efficiency audits we employ the latest innovative cutting edge technologies to dramatically improve light levels, safety, and environment all while helping your business become a leader in the Green economy."},
        {text:"The world is changing and new demands from government, the environment, and clients makes competing in the current business climate fraught with challenges....Luxor energy solutions shines the light so that you can lead the way.  We get big jobs done right."},
        {text:"Our unique process allows us to leverage utility rebates as well as federal and state programs in combination with a deep understanding of energy market and opportunities to provide clients with a customized energy efficiency upgrade with truly unparalleled return on investment."},
       {text: "The savings your business will accrue will be evident from the from the first utility bill after our upgrade and continue year after year.  These substantial savings that coincide with your lighting upgrade are often done with no out of pocket expense at all."},
        {text:"We pride ourselves on the products we deliver with over 95% coming from American owned companies.  While our aesthetic sensibilities are a significant asset, we demand durability along with quality, and our products are designed to last for at least a decade with a minimum of a 5 year guarantee."},    
          ],
    }
  },
  components: {
  },
    props: {
    content: {
        type: String
    }
}
};
</script>
<style scoped>
.holder{
  border-left: black solid 1px;
  border-bottom: black solid 1px;
  font-family: 'Questrial', sans-serif;
  padding: 10px;
  max-width: 400px;
  margin: 5%;
}
</style>