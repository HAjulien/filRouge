<template>
<div>
  <HeaderMobile />
  <Navigation />
  <FooterMobile />
</div>

</template>

<script>
import headerMobile from '~/components/headerMobile.vue'
import navigation from '~/components/navigation.vue'
import footerMobile from '~/components/footerMobile.vue'
export default {
  name: 'IndexPage',
  components: { navigation, headerMobile, footerMobile },
}
</script>

<style lang="scss" >

  
</style>
