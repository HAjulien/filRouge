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

    @media screen and (min-width:766px){

      body::-webkit-scrollbar{
      width: 17px;
      }

    /* Works on Firefox */
      * {
        scrollbar-width: thin;
        scrollbar-color: $principale #bdb1ac80;
      }

    /* Works on Chrome, Edge, and Safari */


      *::-webkit-scrollbar-track {
        background-color: $green;
      }

      *::-webkit-scrollbar-thumb {
        background-color: #edca82;
        border-radius: 20px;
        border: 4px solid #a9c0a6;
      }

    }

    
</style>