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
  <div class="mz-card col-2 align-content-center">
    <img :src="character.img" :alt="character.name">
    <p class="mt-4 fs-5 mb-4 text-center text-uppercase">{{character.name}}</p>
    <p class="mb-1 fs-6 text-center text-secondary">{{character.category}}</p>
    <p class="mb-4 fs-6 text-center text-secondary">{{character.status}}</p>
  </div>
 
</template>



<style lang="scss" scoped>

  @use '../style/partials/variables' as *;

  .mz-card{
    height: 450px;
    background-color: $primary-color;
    justify-content: center;
    margin: 10px 5px;
    img{
      max-width: 99%;
      margin-top: 5px;
    }
  }

</style>