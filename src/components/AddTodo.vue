<template>
  <div class="">
      <h3>Add Todos</h3>
      <div class="add">
        <form @submit="onSubmit">
          <input type="text" v-model="title" placeholder="Add Todo...">
          <input type="submit" value="submit">
        </form>
      </div>
  </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
    name: 'AddTodos',
    data() {
      return {
        title: '',
      }
    },
    methods: {
      ...mapActions(['addTodo']),
      onSubmit(e) {
        e.preventDefault();
        this.addTodo(this.title);
      }
    },
};
</script>

<style lang="scss" scoped>
form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  border: 2px solid #41b883;
  padding: 10px;
  outline: 0;
}
input[type="submit"] {
  flex: 2;
  border: 2px solid #41b883;
  color: white;
  background: #41b883;
  cursor: pointer;
}

</style>