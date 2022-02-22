<template>
  <header>
      
      <MyLogo />

      <nav>
        <ul>
          <li v-for="(link, index) in links" :key="index">
            <a :href="link.url" :class="link.current?'active':''">{{link.text}}</a>
          </li>
        </ul>
      </nav>

  </header>
</template>

<script>
import MyLogo from './partials/MyLogo.vue';

export default {
  name: 'MyHeader',
  components: {
    MyLogo
  },
  data() {
    return {
      links: [
          {
              text: "Home",
              url: "#",
              current: false,
          },
          {
              text: "Prodotti",
              url: "#",
              current: true,
          },
          {
              text: "Chi Siamo",
              url: "#",
              current: false,
          },
          {
              text: "Contatti",
              url: "#",
              current: false,
          },
      ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../assets/style/variables.scss";

header {
  text-align: center;
}

ul {
  margin: 30px 0px;

  li {
    display: inline-block;

    a {
      text-decoration: none;
      color: #000;
      padding: 20px;

      // li a.active
      // li a:hover
      &.active, 
      &:hover {
        background-color: $secondaryColor;
      }

    }
  }
  
}



</style>
