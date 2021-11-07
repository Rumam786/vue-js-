<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <login /> -->
    <!-- <create /> -->
    <!-- <mount /> -->
    <employes />
    <!-- <post /> -->
    <div v-if="display">
      <!-- <destroy /> -->
      <!-- <activeboot /> -->
    </div>
    <!-- <button v-on:click="toogle">toogle</button> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import login from './components/login.vue'
// import create from './components/create.vue'
// import mount from './components/mount.vue'
// import destroy from './components/destroy.vue'
// import activeboot from './components/activeboot.vue'
import employes from './components/employes.vue'
// import post from './components/post.vue'
export default {
  name: 'App',
  components: {
    // HelloWorld,
    // login,
    // create,
    // mount,
    // destroy,
    // activeboot,
    employes,
    // post
  },
  data() {
    return {
      display: true
    }
  },
  methods: {
    toogle() {
      this.display=!this.display
    }
  },
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
