<template>
  <div>
    <button v-bind:class="{ warning: type==='warning', primary: type==='primary' }">{{name}}</button>
  </div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    name: String,
    type: String
  }
}
</script>

<style scoped>
  .primary{
    background-color: blue;
  }
  .warning{
    background-color: red;
  }
</style>
