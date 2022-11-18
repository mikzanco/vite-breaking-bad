<script>

import {store} from '../data/store'

export default {
  name: 'AppHeader',
  props:{
    title: String
  },
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <header class="d-flex">
    <div class="container py-4 d-flex d-block">
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