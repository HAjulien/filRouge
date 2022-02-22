<template>
<div>


  <BannerDesktop/>
   <div class="row">

    <Feature v-for="(feature,index) in features" :key="index" :titre="feature.titre" :image="feature.image" :paragraphe="feature.paragraphe" :button="feature.button" />
   </div>


</div>
</template>

<script>

import axios from 'axios'
import bannerDesktop from '~/components/bannerDesktop.vue'
import feature from '~/components/feature.vue'

export default {
  name: 'IndexPage',
  components: { bannerDesktop, feature },

  data(){
        return {
            features:[],
            errors: []
        }
  },
  // Fetches posts when the component is created.
  created() {
    axios.get(`http://localhost:3000/features.json`)
    .then(response => {
      // JSON responses are automatically parsed.
      this.features = response.data.features
    })
    .catch(e => {
      this.errors.push(e)
    })
  },

   head: {
    title: "MIAM | Nouvelle Cantine de l'AFPA de Créteil",
    meta: [
      {
        hid: 'home',
        name: 'IndexPage',
        content: "Venez découvrir les délicieux plats du Chef Michael Dellore, cuisinés qu'avec des produits frais. Vous pouvez commander à emporter sur notre site."
      }
    ]
  }
}
  
</script>

<style lang="scss" >

  
</style>
