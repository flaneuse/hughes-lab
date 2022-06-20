<template>
<div id="app">
  <div id="nav">
    <router-link to="/">home</router-link> |
    <router-link :to="link.url" class="mr-2" v-for="(link, lIdx) in links" :key="lIdx">{{link.name}}</router-link>
  </div>
  <router-view />
</div>
</template>

<script>
// import Vue from "vue";
export default {
  name: "LocationReportComponent",
  data() {
    return ({
      links: [{
          name: "research",
          url: "/research"
        },
        {
          name: "people",
          url: "/people"
        },
        {
          name: "publications",
          url: "/publications"
        },
        {
          name: "code",
          url: "/code"
        },
        {
          name: "news",
          url: "/news"
        }
      ]
    })
  }
}
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

#nav {
    padding: 30px;

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
            color: #42b983;
        }
    }
}
</style>
