<template>
  <div>
    <div v-for="(todo, index) in list" :key="index">
      {{ todo.type }}   {{ todo.text }}
    </div>
  </div>
</template>

<script>
export default {
  props: ['list']
}
</script>

<style scoped>

</style>
