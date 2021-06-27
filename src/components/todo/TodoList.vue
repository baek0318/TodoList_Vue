<template>
  <div id="todo-list">
    <ul>
      <TodoForm v-for="todo in todos" v-bind:todo-item="todo.text" v-bind:key="todo.id"></TodoForm>
    </ul>
  </div>
</template>

<script>
import TodoForm from "@/components/todo/TodoForm";

export default {
  el: '#todo-list',
  props: ['items'],
  data: function () {
    return {
      todos: this.items
    }
  },
  components: {
    'TodoForm': TodoForm
  }
}
</script>

<style>
#todo-list {
  background-color: #2f4153;
}
</style>