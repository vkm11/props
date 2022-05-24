<template>
  <div id="app">
    <h1>Props in Vue js</h1>
    <Child v-bind:users="users" />
    <br>
    <h1>{{title}}</h1>
    <Child_parent v-on:changeTitle="updateTitle($event)" />
  </div>
</template>

<script>
import Child from "./components/Child";
import Child_parent from './components/Child_parent';
export default {
  name: "App",
  components: {
    Child,
    Child_parent
  },
  // data(){
  //  return {users:[
  //    {name:"Vijay", email:"vijay@gmail.com"},
  //    {name:"Gokul",email:"gokul@gmail.com"},
  //    {name:"Nithin",email:"nithin@gmail.com"},
  //    {name:"Prajwal",email:"prajwal@gmail.com"}
  //    ]}
  // },

  // Child to parent (Child_parent)
  data(){
     return {title:"Props tutorial"}
  },
  methods:{
    updateTitle(title){
      this.title=title
    }
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
