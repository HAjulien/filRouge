<template>
<div>
  <BannerDesktop/>
  <Features/>
</div>

</template>

<script>

import features from '~/components/features.vue'
import bannerDesktop from '~/components/bannerDesktop.vue'

export default {
  name: 'IndexPage',
  components: { features, bannerDesktop },
}
</script>

<style lang="scss" >

  
</style>
