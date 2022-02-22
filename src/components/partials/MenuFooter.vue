<template>
  <div>
      <h3>{{title}}</h3>
      <nav>
          <ul>
              <li v-for="(item, index) in items" :key="index">
                  <a :href="item.src">{{item.text}}</a>
              </li>
          </ul>
      </nav>
  </div>
</template>

<script>
    export default {
        name: "MenuFooter",
        props: ["title", "items"]
    }
</script>

<style>

</style>