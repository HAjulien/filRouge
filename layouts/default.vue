<template>
    <div class="App">
        <HeaderMobile />
        <HeaderDesktop />
        <Nuxt />
        <Navigation />
        <FooterMobile />
    </div>
</template>

<script>

import headerMobile from '~/components/headerMobile.vue'
import headerDesktop from '~/components/headerDesktop.vue'
import navigation from '~/components/navigation.vue'
import footerMobile from '~/components/footerMobile.vue'


export default {
  name: 'AppPage',
  components: { navigation, headerMobile, headerDesktop, footerMobile },
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