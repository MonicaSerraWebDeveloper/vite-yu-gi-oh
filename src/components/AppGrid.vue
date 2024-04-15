<script>
    import { store } from '../store.js'
    import AppCard from './AppCard.vue'

    export default {
        name: 'AppGrid',
        components: {
            AppCard
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
                <AppCard v-for="card in store.cards"></AppCard>
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