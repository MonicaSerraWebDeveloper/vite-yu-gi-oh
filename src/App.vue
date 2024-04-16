<script>
  import AppHeader from './components/AppHeader.vue'
  import AppGrid from './components/AppGrid.vue'
  import AppLoading from './components/AppLoading.vue'
  import AppSelectFilter from './components/AppSelectFilter.vue'
  import { store } from './store.js'
  import axios from 'axios'

  export default {
    components: {
      AppHeader,
      AppGrid,
      AppLoading,
      AppSelectFilter
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
          store.cards = response.data.data;
          store.isLoading = false;
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
    <AppSelectFilter></AppSelectFilter>
    <AppGrid v-if="store.isLoading === false"></AppGrid>
    <AppLoading v-else></AppLoading>
  </main>

</template>

<style lang="scss">
  @use './style/generic';

  main {
    background-color: #d48f38;
  }

</style>