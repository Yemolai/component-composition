<template>
  <input
    class="input-proton"
    :type="type"
    v-model="value"
    @input="$emit('input', value)">
</template>
<script>
export default {
  name: 'InputProton',
  props: {
    type: {
      type: String,
      default: 'text'
    },
    value: {
      type: String
    }
  }
}
</script>
<style>
/* no style allowed in a proton */
</style>

