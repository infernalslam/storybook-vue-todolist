<template>
  <div class="hello">
    TODOLIST
    <input-list :types="types" :submit="submit"></input-list>
    <todo-list :list="list"></todo-list>
  </div>
</template>

<script>
import inputList from './InputList'
import todoList from './TodoList'
export default {
  name: 'Index',
  components: {
    inputList,
    todoList
  },
  data () {
    return {
      list: [],
      types: [
        '🏭',
        '😷',
        '⚽️'
      ]
    }
  },
  methods: {
    submit (type, text) {
      this.list.push({ type, text })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
