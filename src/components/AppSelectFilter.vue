<script>

    export default {
        name: 'AppSelectFilter'
    }

</script>

<template>
    <div class="container">
        <select name="archetype" id="archetype">
            <option value="test">test</option>
            <option value="test">test</option>
            <option value="test">test</option>
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
        }
    }
</style>