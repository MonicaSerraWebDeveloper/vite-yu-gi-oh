<script>
  import AppHeader from './components/AppHeader.vue'
  import AppGrid from './components/AppGrid.vue'

  export default {
    components: {
      AppHeader,
      AppGrid
    }
  }

</script>

<template>

  <AppHeader></AppHeader>
  <main>
    <AppGrid></AppGrid>
  </main>

</template>

<style lang="scss">
  @use './style/generic';

</style>