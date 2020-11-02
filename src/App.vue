<template>
  <div id="app">
    <Login username="Baptiste"/>
    <Product/>
  </div>
</template>

<script>
  import Login from './components/Login.component.vue'
  import Product from './components/Product.component.vue'

  export default {
    name: 'App',
    components: {
      Login,
      Product
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 8px;
}
</style>
