<script>
    import { store } from '../store.js'
    import AppCard from './AppCard.vue'
    import AppBannerTop from './AppBannerTop.vue'

    export default {
        name: 'AppGrid',
        components: {
            AppCard,
            AppBannerTop
        },
        data() {
            return {
                store
            }
        }
    }

</script>

<template>
    <div class="bg-container">
        <div class="container">
            <div class="row">
                <AppBannerTop></AppBannerTop>
                <AppCard v-for="card in store.cards" :key="card.id" :singleCard="card"></AppCard>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    .bg-container {
        background-color: #d48f38;
        padding: 50px 0;

        .container {
            background-color: #fff;
            padding: 30px;

            .row {

            margin: 0 -10px -30px;
        }
    }
}
</style>