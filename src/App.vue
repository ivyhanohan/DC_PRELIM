<template>
  <div id="app">
    <ItemList />
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue'

export default {
  name: 'App',
  components: {
    ItemList
  }
}
</script>
<!-- 
<style>
/* Add global styles here if needed */
</style> -->

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #021A02FF;
  margin-top: 60px;
  background-color: #728F9CFF;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  padding: 20px;
}
</style>