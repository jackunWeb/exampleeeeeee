<template>
  <div id="app">
    {{info}}
  </div>
</template>

<script>
import axios from "axios"

export default {
  name: 'App',
  data:()=>({
    info:null
  }),
  mounted:function(){
    axios
      .get(document.URL+'api/foo')
      .then(response => (this.info = response.data.msg));
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
