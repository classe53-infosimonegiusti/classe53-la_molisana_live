<template>
    <footer>

      <div class="flex">
        <MyLogo/>
        <MenuFooter title="PASTIFICIO" :items="menuPastificio"/>
        <MenuFooter title="PRODOTTI" :items="menuProdotti"/>
      </div>
      
      
      <img class="mointains" :src="require('../assets/img/footer-montagne-bottom.jpg')">

    </footer>
</template>

<script>

import MyLogo from './partials/MyLogo.vue';
import MenuFooter from './partials/MenuFooter.vue';

export default {
  name: 'MyFooter',
  components: {
    MyLogo,
    MenuFooter
  },
  data() {
    return {
      menuPastificio: [
        {
          src: "#",
          text: "Il pastificio"
        },
        {
          src: "#",
          text: "Grano"
        },
        {
          src: "#",
          text: "Filiera"
        }
      ],
      menuProdotti: [
        {
          src: "#",
          text: "Le classiche"
        },
        {
          src: "#",
          text: "Le Integrali"
        },
        {
          src: "#",
          text: "Le Speciali"
        }
      ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  footer {
    .mointains {
      width: 100%
    }
    .flex {
      display: flex;
      justify-content: space-between;
    }
  }
</style>
