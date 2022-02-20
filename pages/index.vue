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
}
</script>

<style lang="scss" >

  
</style>
