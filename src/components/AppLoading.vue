<script>

    export default {
        name: 'AppLoading'
    }

</script>

<template>

    <div class="load-container">
        <div class="loader"></div>
        <div class="text-load">Loading...</div>
    </div>

</template>

<style scoped lang="scss">

    .load-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 20px;
        height: calc(100vh - 60px);

        .text-load {
            font-size: 40px;
        }
        .loader {
            border: 16px solid #f3f3f3;
            border-top: 16px solid blue;
            border-radius: 50%;
            width: 150px;
            height: 150px;
            animation: spin 2s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    }
</style>