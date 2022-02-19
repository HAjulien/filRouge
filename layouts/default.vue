<template>
    <div class="App">
        <HeaderMobile />
        <Nuxt />
        <Navigation />
        <FooterMobile />
    </div>
</template>

<script>

import headerMobile from '~/components/headerMobile.vue'
import navigation from '~/components/navigation.vue'
import footerMobile from '~/components/footerMobile.vue'


export default {
  name: 'AppPage',
  components: { navigation, headerMobile, footerMobile },
}


</script>

<style lang="scss">
    *{
      margin: 0;
      padding: 0;
    }  

    *::before, *::after{
      box-sizing: border-box;
    }
</style>