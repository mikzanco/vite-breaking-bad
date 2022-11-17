<script>
export default {
  name: 'CharacterCard',
  props:{
    character: Object
  }
}
</script>

<template>
<!-- img name category  status -->
  <div class="mz-card col-2">
    <img :src="character.img" :alt="character.name">
    {{character.name}}
  </div>
 
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;

  .mz-card{
    height: 300px;
    background-color: $primary-color;
    justify-content: center;
    margin: 10px 5px;
    img{
      max-width: 99%;
      margin-top: 10px;
    }
  }

</style>