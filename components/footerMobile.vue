<template>
    <footer class="footerMobile px-2 bg-gray-200 ">

        <p class="text-center"> nous suivre sur :</p>
        <ul class=" flex justify-around">
            <li><a href="https://www.facebook.com" target="_blank"><font-awesome-icon :icon="['fab', 'facebook']" class="fa-2x" /></a>
 </li>
            <li><a href="https://www.instagram.com" target="_blank"><font-awesome-icon :icon="['fab', 'instagram']" class="fa-2x" /></a>
 </li>
            <li><a href="https://twitter.com" target="_blank"><font-awesome-icon :icon="['fab', 'twitter']" class="fa-2x" /></a> </li>
        </ul>
        <p class="text-center">CANTINE MIAM tous droits réservés, 2022</p>
        <div>
            <transition name="bounce">
            <p v-if="active" class="test"><HeaderMobile /></p>
            </transition>
            <button @click="active = !active" >Toggle active</button>
        </div>
        

    </footer>
</template>

<script>

import headerMobile from '~/components/headerMobile.vue'

export default {
  name: 'FooterMobile',
  components: { headerMobile },
  data(){
      return{
          active: false,
      }
  },
}
</script>

<style lang="scss" scoped>
   
    .bounce-enter-active{
        animation: bounce-in .5s;
    }
    .bounce-leave-active{
        animation: bounce-in .5s reverse;
    }
    @keyframes bounce-in{
        0%{
            transform: scale(0);
        }
        50%{
            transform: scale(1.5);
        }
        100%{
            transform: scale(1);
        }
    }
</style>