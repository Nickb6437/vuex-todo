<template>
  <div id="app">
    <div class="container">
      <AddTodo />
      <FilterTodos />
      <Todo />
    </div>
  </div>
</template>

<script>
import Todo from './components/Todo.vue'
import AddTodo from './components/AddTodo.vue'
import FilterTodos from './components/FilterTodos.vue'

export default {
  name: 'App',
  components: {
    Todo,
    AddTodo,
    FilterTodos,
  },
}
</script>

<style lang="scss">
body {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    line-height: 1.6;
    background: #e8f7f0;
}
.container {
    min-width: 1100px;
    margin: auto;
    overflow: auto;
    padding: 0 2rem;
}
</style>
