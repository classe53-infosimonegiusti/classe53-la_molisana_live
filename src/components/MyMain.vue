<template>
    <section class="products">

      <h1>Lista prodotti</h1>

      <div class="container">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa, at quasi unde ea voluptas eveniet, odio nesciunt molestias quidem animi fuga cum temporibus earum laborum, omnis quam cupiditate. Pariatur, numquam.
      </div>

    </section>
</template>

<script>
export default {
  name: 'MyMain',
 
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
  }

}

</style>
