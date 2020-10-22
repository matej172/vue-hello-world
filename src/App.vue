<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to My Vue.js App" poznamka="Toto je webte1 prednáška"/>
  <HelloTable rows=5 cols=8></HelloTable>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";
import HelloTable from "@/components/HelloTable";

export default {
  name: 'App',
  components: {
    HelloTable,
    HelloWorld
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
  margin-top: 60px;
}
</style>
