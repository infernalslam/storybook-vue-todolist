<template>
  <div class="columns is-gapless">
    <div class="column is-2">
      <div class="select">
        <select v-model="type">
          <option v-for="(type, index) in types" :key="index" :value="type"> {{ type }} </option>
        </select>
      </div>
    </div>
    <div class="column">
      <input class="input is-rounded" type="text" placeholder="todolist...." v-model="text" @keyup.enter="submit(type, text)">
    </div>
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
