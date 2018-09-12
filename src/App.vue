<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <VueTable name="mike erickson" dob="10-15-1966"/>
  </div>
</template>

<script>
  import VueTable from "./components/VueTable.vue";

  export default {
    name: "app",
    components: {
      VueTable
    }
  };
</script>

<style scoped lang="scss">
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
