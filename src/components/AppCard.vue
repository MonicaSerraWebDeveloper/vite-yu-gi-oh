<script>

export default {
    name: 'AppCard',
    props: {
        singleCard: Object
    }
}

</script>

<template>

    <div class="card">
        <div class="image-container">
            <img src="https://images.ygoprodeck.com/images/cards_small/34541863.jpg" alt="">
        </div>
        <div class="text-container">
            <h3>Nome carta</h3>
            <div class="archetipo-text">Archetipo</div>
        </div>
    </div>


</template>

<style scoped lang="scss">


        .card {
        background-color: #d48f38;
        width: calc((100% / 5) - 20px);
        margin: 0 10px 30px;
        

        .image-container {
            
            img {
                width: 100%;
            }
        }

        .text-container {
            padding: 25px;
            text-align: center;
            color: #fff;

            h3 {
                text-transform: uppercase;
                margin-bottom: 20px;
            }

            .archetipo-text {
                color: #000;
            }
        }
    }
    

</style>