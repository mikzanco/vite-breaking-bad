<script>

import {store} from '../data/store'
import CharacterCard from './CharacterCard.vue'

export default {
  name: 'AppCharacterList',
  components:{
    CharacterCard
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

    <CharacterCard 
    v-for="character in store.characterListData" 
    :key="character.char_id" 
    :character="character"

    />
    
  </div>
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;

</style>