<script>

import axios from 'axios'
import {store} from './data/store'

import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import AppSearch from './components/AppSearch.vue'
import AppCharacterList from './components/AppCharacterList.vue'



export default {
  name: 'App',
  data(){
    return{
      store
    }
  },
  components:{
    AppHeader,
    AppMain,
    AppFooter,
    AppSearch,
    AppCharacterList

  },
  methods:{
    getCharacter(){
      axios.get(store.apiUrl)
        .then(result =>{
          
          store.characterListData = result.data
          console.log(store.characterListData);
        })
        .catch(error =>{
          console.log(error);
        })
    }
  },
  mounted(){
    this.getCharacter()
  }
}
</script>

<template>

  <AppHeader title="Breaking Bad Api" />
  <main>
    <AppSearch  />
    <AppCharacterList />
  </main>
  

</template>



<style lang="scss">
  @use './style/general';
</style>
