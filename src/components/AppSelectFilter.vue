<script>
    import { store } from '../store.js'

    export default {
        name: 'AppSelectFilter',

        data() {
            return {
                store
            }
        }
    }

</script>

<template>
    <div class="container">
        <select name="archetype" id="archetype">
            <option selected value="empty">-- Archetipo --</option>
            <option v-for="archetype in store.archetypes" value="archetype.archetype_name">{{archetype.archetype_name}}</option>
        </select>
    </div>
</template>

<style scoped lang="scss">

    .container {
        padding: 50px 0 0;

        #archetype {
            padding: 5px;
            width: 150px;
            height: 35px;
            border-radius: 5px;
            border: 1px solid #ccc;
            outline: none;
        }
    }
</style>