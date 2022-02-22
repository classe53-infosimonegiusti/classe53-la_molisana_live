<template>
  <div id="app">
    <MyHeader/>
    <MyMain />
    <MyFooter />

    <MiaProva pippo="Tutto bene, tu?!" messaggio="Ciao come stai?"/>

  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';

//Caso più semplice possibile solo per fini didattici
import MiaProva from './components/partials/MiaProva.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter,
    MiaProva
  }
}
</script>

<style lang="scss">

  @import "./assets/style/general.scss";

</style>
