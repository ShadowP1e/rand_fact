<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" height=150px width=150px>
    <helloWorld v-bind:value="helloWorld" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      helloWorld: {
        fact: '',
      }
    }
  },
  methods:{
    getFact(){
      this.axios.get('http://188.225.47.187/api/cats/random-fact.php')
        .then((response)=>{
          this.helloWorld.fact = response.data;
        })
    }
  },
  mounted(){
    this.getFact();
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
