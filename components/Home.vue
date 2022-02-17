<template>
<div class="home bg-red-300">
    <h1 class="text-red-700	"> test</h1>
  <p class="text-red-700">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis voluptatibus tempore corrupti odio blanditiis dolores optio sunt! Beatae tempora impedit facilis, explicabo unde ex quas fugit autem necessitatibus. Totam, in!</p>
</div>
</template>

<script>
export default {
  name: 'HomePage',
}
</script>

<style lang="scss" scoped>
    .home{
        position: relative;
        height: 300px;
    }
  p{
    color: $green;
  @include absolutePosition(45%,25%,35%,25%);
}
  
</style>