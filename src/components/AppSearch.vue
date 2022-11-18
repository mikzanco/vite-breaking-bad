<script>

import {store} from '../data/store'

export default {
  name: 'AppSearch',
  data(){
    return{
      store 
    }
  }
}
</script>


<template>

  <div class="col.auto">
    <input v-model="store.characterToSearch" type="text" class="form-control" placeholder="Cerca un personaggio">
  </div>
  <div class="col-2 m-2 align-items-center d-flex">
      <select v-model="store.categoryToSearch" class="form-select" aria-label="Default select example">
        <option value="" selected>Select category</option>       
        <option value="Breaking Bad">Breaking Bad</option>
        <option value="Better Call Saul">Better call Saul</option>
      </select>
    </div>
    <button @click="$emit('startSearch')" class="btn btn-outline-primary">Search</button>
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;

</style>