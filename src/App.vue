<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppSearch from './components/AppSearch.vue';
import AppCharacterList from './components/AppCharacterList.vue'; 



export default {
  name: 'App',
  components:{
    AppHeader,
    AppMain,
    AppFooter,
    AppSearch,
    AppCharacterList

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
