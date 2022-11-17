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
  <header>
    <div class="container py-4 d-flex">
      <img src="/logo.svg" alt="">
      <h1>{{title}}</h1>
    </div>
    <div class="input-group mx-5 mb-3">
      <button class="btn btn-outline-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="true">Select a Category</button>
        <ul class="dropdown-menu">
          <li><a class="dropdown-item" href="#">Action</a></li>
          <li><a class="dropdown-item" href="#">Another action</a></li>
          <li><a class="dropdown-item" href="#">Something else here</a></li>
          <li><hr class="dropdown-divider"></li>
          <li><a class="dropdown-item" href="#">Separated link</a></li>
        </ul>
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