<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <material-input v-model="text"/>
    <p>{{ text }}</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MaterialInput from '@/components/atom/material-input.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    MaterialInput
  },
  data () {
    return {
      text: 'asdasd'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
