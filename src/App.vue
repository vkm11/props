<template>
  <div id="app">
    <h1>Props in Vue js</h1>
    <Child v-bind:users="users" />
  </div>
</template>

<script>
import Child from "./components/Child";

export default {
  name: "App",
  components: {
    Child,
  },
  data(){
   return {users:[
     {name:"Vijay", email:"vijay@gmail.com"},
     {name:"Gokul",email:"gokul@gmail.com"},
     {name:"Nithin",email:"nithin@gmail.com"},
     {name:"Prajwal",email:"prajwal@gmail.com"}
     ]}
  }
};
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
