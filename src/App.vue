<template>
  <div id="app">
    <material-input-field v-model="text" :size="txtSize"/>
    <br/>
    <input-atom v-model="text"/>
    <br>
    <material-input v-model="text"/>
    <br/>
    <v-text>{{ text }}</v-text>
    <br/>
    <div v-for="i in 6" :key="i">
      <v-text :el="'h' + i">{{text}}</v-text>
    </div>
  </div>
</template>

<script>
import VText from '@/components/VText.vue'
import InputAtom from '@/components/atom/input-atom'
import MaterialInputField from '@/components/material-input-field.vue'
import MaterialInput from '@/components/atom/material-input.vue'

export default {
  name: 'app',
  components: {
    VText,
    InputAtom,
    MaterialInput,
    MaterialInputField
  },
  data () {
    return {
      txtSize: 1,
      text: 'Atomic Design'
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
