<template>
    <header class="headerMobile flex justify-between items-center px-2 bg-gray-600 h-16">
      <img src="~/assets/images/test.png" class="w-24 h-10" />
       <span class="profil bg-red-500 w-36 flex justify-center items-center rounded-xl mt-2">
        <nuxt-link to=""> <svg 
       version="1.0" xmlns="http://www.w3.org/2000/svg"  width="28.000000pt" height="28.000000pt" viewBox="0 0 32.000000 32.000000"  preserveAspectRatio="xMidYMid meet">  
       <g transform="translate(0.000000,32.000000) scale(0.100000,-0.100000)" fill="#000000" stroke="none"> <path d="M83 280 c-85 -51 -81 -179 6 -225 116 -60 239 71 171 182 -37 61 -116 81 -177 43z m117 -15 c50 -26 71 -85 50 -139 l-9 -25 -29 27 c-19 18 -25 31 -19 39 14 19 0 61 -23 68 -11 3 -29 3 -40 0 -23 -7 -37 -49 -23 -68 6 -8 0 -21 -19 -39 l-29 -27 -9 25 c-14 35 -12 60 5 94 28 54 90 73 145 45z m-25 -75 c0 -18 -6 -26 -23 -28 -13 -2 -25 3 -28 12 -10 26 4 48 28 44 17 -2 23 -10 23 -28z m25 -76 c21 -21 22 -27 10 -35 -36 -23 -84 -23 -120 0 -12 8 -11 14 10 35 14 15 35 26 50 26 15 0 36 -11 50 -26z"/> </g> 
         </svg></nuxt-link>
         <nuxt-link to="#" class="text-xs"> Se connecter </nuxt-link>
       </span>

    </header>
</template>

<script>
export default {
  name: 'HeaderMobile',
}
</script>

<style lang="scss" scoped>
   
  
</style>