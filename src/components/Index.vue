<template>
  <div>
    
    <div class="columns is-mobile">
      <div class="column is-half is-offset-one-quarter">
        <input-list :types="types" :submit="submit"></input-list>
      </div>
    </div>

    <div class="columns is-mobile">
      <div class="column is-half is-offset-one-quarter">
        <todo-list :list="list"></todo-list>
      </div>
    </div>

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
