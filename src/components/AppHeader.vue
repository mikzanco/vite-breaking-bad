<script>
export default {
  name: 'AppHeader',
}
</script>

<template>
  <header>
    <img src="/logo.svg" alt="">
    <h1>Breaking Bad Api</h1>
  </header>
  
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;
  header{
    display: flex;
    img{
    width: 100px;
    height: 50px;
    }
    h1{
      font-weight: 500 ;
    }
  }
  

</style>