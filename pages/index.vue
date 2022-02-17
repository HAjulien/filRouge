<template>
<div>
  <Header />
  <Navigation />
</div>

</template>

<script>
import header from '~/components/header.vue'
import navigation from '~/components/navigation.vue'
export default {
  components: { navigation, header },
  name: 'IndexPage',
}
</script>

<style lang="scss" >

  
</style>
