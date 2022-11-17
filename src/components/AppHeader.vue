<script>
export default {
  name: 'AppHeader',
  props:{
    title: String
  }
}
</script>

<template>
  <header>
    <div class="container py-2 d-flex">
      <img src="/logo.svg" alt="">
      <h1>{{title}}</h1>
    </div>
    
  </header>
  
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;

  header{
    img{
    width: 100px;
    height: 50px;
    }
    h1{
      font-weight: 500 ;
    }
  }
  

</style>