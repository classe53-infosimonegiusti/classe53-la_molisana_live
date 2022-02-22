<template>
    <section class="products">

      <h1>Lista prodotti</h1>

      <div class="container">
        <ProductCard 
          v-for="(product, index) in products" 
          :key="index"
          :titolo="product.titolo"
          :src="product.src"
        />
        <!--
          <div class="product" v-for="(product, index) in products" :key="index">
              <img :src="product.src" :alt="product.titolo">
              <h3>{{product.titolo}}</h3>
          </div>
        -->
      </div>

    </section>
</template>

<script>

import ProductCard from './partials/ProductCard.vue';

export default {

  name: 'MyMain',
  components: {
    ProductCard
  },
  data() {

      return {

        products: [
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
            titolo: "N.4 Spaghetto Quadrato Bucato",
            tipo: "lunga",
            cottura: 6,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
            titolo: "N.5 Fettuccine",
            tipo: "lunga",
            cottura: 13,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
            titolo: "N.6 Linguine",
            tipo: "lunga",
            cottura: 12,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
            titolo: "N.7 Mezze Linguine",
            tipo: "lunga",
            cottura: 11,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
            titolo: "n.11 Spaghettino Quadrato",
            tipo: "lunga",
            cottura: 9,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
            titolo: "N.38 Mezze maniche",
            tipo: "corta",
            cottura: 12,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
            titolo: "N.44 Sedani",
            tipo: "corta",
            cottura: 8,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
            titolo: "N.49 Sedanini",
            tipo: "corta",
            cottura: 8,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
            titolo: "N.53 Lumachine",
            tipo: "corta",
            cottura: 12,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
            titolo: "N.55 Chifferi rigati",
            tipo: "corta",
            cottura: 12,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
            titolo: "N.58 Misto corto",
            tipo: "corta",
            cottura: 9,
          },
          {
            src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
            titolo: "N.84 Ditale Quadrato",
            tipo: "cortissima",
            cottura: 12,
          },
        ]

      }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../assets/style/variables.scss";

.products {

  background-image: url('../assets/img/fondo-pag-speciali.jpg');

  h1 {
    text-align: center;
    color: $primaryColor;
    padding: 30px 0px;
  }

  .container {
    min-height: 300px;
    padding: 50px;
    display: flex;
    flex-wrap: wrap;
  }


}

</style>
