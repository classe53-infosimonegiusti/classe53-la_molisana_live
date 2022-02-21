<template>
  <header>
      <a href="#">
        <img src="../assets/img/la-molisana-logo.png">
      </a>

      <nav>
        <ul>
          <li v-for="(link, index) in links" :key="index">
            <a :href="link.url">{{link.text}}</a>
          </li>
          <!--
          <li>
            <a class="active" href="#">Prodotti</a>
          </li>
           <li>
            <a href="#">Chi Siamo</a>
          </li>
           <li>
            <a href="#">Contatti</a>
          </li>
          -->
        </ul>
      </nav>

  </header>
</template>

<script>
export default {
  name: 'MyHeader',
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
