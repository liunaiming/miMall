<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import axios from 'axios'
import jsonp from 'jsonp'
export default {
  name: 'App',
  components: {

  },
  data(){
    return {
      age:30,
      data:''
    }
  },

   mounted(){
  let url = "/activity";
  jsonp(url,(error,res)=>{
    if(error){
      let result = res
      this.data = result
    }
    
})
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
