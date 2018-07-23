<template>
  <div>
    <select v-model="type">
      <option v-for="(type, index) in types" :key="index" :value="type"> {{ type }} </option>
    </select>
    <input type="text" v-model="text" @keyup.enter="submit(type, text)">
  </div>
</template>

<script>
export default {
  props: ['form', 'types', 'submit'],
  data () {
    return {
      type: this.types[0],
      text: ''
    }
  }
}
</script>

<style scoped>
</style>
