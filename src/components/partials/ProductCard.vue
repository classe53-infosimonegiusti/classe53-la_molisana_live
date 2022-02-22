<template>
   <div class="product">
        <img :src="src" :alt="titolo">
        <h3>{{titolo}}</h3>
        <h1>{{pippo}}</h1>
    </div>
</template>

<script>
    export default {
        name: 'ProductCard',
        props: {
            "titolo": String, 
            "src": String
        },
        data() {
            return {
                'pippo' : 'ciaoMondo'
            }
        }
    }
</script>

<style scoped lang="scss">

    @import "../../assets/style/variables.scss";

    .product {
        width:25%;
        border: solid 2px $secondaryColor;
        min-height: 250px;
        background-color: white;
        padding: 15px;

        h3 {
            text-align: center;
            color: $primaryColor;
            font-size: 18px;
        }

        img {
            width: 100%;
        }
    }

</style>