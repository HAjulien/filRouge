<template>
<div>
  <BannerDesktop/>
  <Features/>
</div>

</template>

<script>

import bannerDesktop from '~/components/bannerDesktop.vue'
import features from '~/components/features.vue'

export default {
  name: 'IndexPage',
  components: { bannerDesktop, features },

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
