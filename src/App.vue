<script>
  import AppHeader from './components/AppHeader.vue'
  import AppGrid from './components/AppGrid.vue'
  import { store } from './store.js'
  import axios from 'axios'

  export default {
    components: {
      AppHeader,
      AppGrid,
    },

    data() {
      return {
        store
      };
    },

    methods: {
      cardsFromApi() {

        const queryParams = {
          num: 20,
          offset: 0
        };

        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
          params: queryParams
        })
        .then((response) => {
          store.cards = response.data.data
        })
      }
    },
    mounted() {
      this.cardsFromApi()
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