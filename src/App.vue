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
      store.isLoaded = false;
      axios.get(store.apiUrl, {
        params:{
          name: store.characterToSearch,
          category: store.categoryToSearch
        }
      })
        .then(result =>{
          
          store.characterListData = result.data
          store.isLoaded = true;
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
    <AppSearch @startSearch="getCharacter()" />
    <AppCharacterList />
  </main>
  

</template>



<style lang="scss">
  @use './style/general';
</style>
