<script>

import {store} from '../data/store'
import CharacterCard from './CharacterCard.vue'
import AppLoading from './AppLoading.vue'

export default {
  name: 'AppCharacterList',
  components:{
    CharacterCard,
    AppLoading
  },
  data(){
    return{
      store
    }
  }
}
</script>


<template>
  
  <div class="container">
    <div class="numberChar d-flex align-items-center p-4">
      Found ... characters
    </div>
    <div v-if="store.isLoaded" class="row d-flex justify-content-around">
      <CharacterCard 
        v-for="character in store.characterListData" 
        
        :key="character.char_id" 
        :character="character"
      />
    </div>
    <div v-else>
        
    </div>
    

  </div>
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;

  .container{
    width: 80%;
    background-color: white;
    padding: 10px;
    .numberChar{
      height: 60px;
      width: 80%;
      background-color: $primary-color;
      margin: 50px auto;
    }
  }

</style>