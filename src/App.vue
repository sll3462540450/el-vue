<template>
  <div id="app">
    <!-- <div id="nav"> 
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div> -->
    <Nav/>
    <router-view />
  </div>
</template>
<script>
import Nav from './views/Nav'
export default {
  components:{
    Nav
  },
  data() {
    return {
     
    };
  }
};
import "./assets/index.css";
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
