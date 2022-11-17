<script>
export default {
  name: 'CharacterCard',
  props:{
    character: Object
  }
}
</script>

<template>

  <div class="mz-card">
    {{character.name}}
  </div>
 
</template>



<style lang="scss" scoped>

</style>