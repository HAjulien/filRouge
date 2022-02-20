<template>

<ul class=" md:hidden navigation flex items-center justify-between bg-red-200 p-1 rounded-lg" >
  <li class="flex-1 mr-2">
    <NuxtLink to="/" class="text-center block border-blue-500 rounded py-2 px-4 bg-blue-500 hover:bg-blue-700 text-white" >Accueil </NuxtLink>
  </li>
  <li class="flex-1 mr-2">
    <NuxtLink to="/" class="text-center block rounded hover:border-gray-200 text-blue-500 hover:bg-gray-200 py-2 px-4" > Horaires</NuxtLink>
  </li>
    <li class="flex-1 mr-2">
    <NuxtLink to="/" class="text-center block rounded hover:border-gray-200 text-blue-500 hover:bg-gray-200 py-2 px-4" > click&collect</NuxtLink>
  </li>
  <li class="flex-1 mr-2">
    <NuxtLink to="/" class="text-center block rounded hover:border-gray-200 text-blue-500 hover:bg-gray-200 py-2 px-4" > Menu</NuxtLink>
  </li>
</ul>


</template>

<script>
export default {
  name: 'NavigationPage',
}
</script>

<style lang="scss" scoped>


  .navigation{
    position: sticky;
    bottom:0%;
  }
  
</style>