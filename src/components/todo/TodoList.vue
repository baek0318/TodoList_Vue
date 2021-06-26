<template>
  <div id="todo-list">
    <ul>
      <TodoForm v-for="todo in todos"></TodoForm>
    </ul>
  </div>
</template>

<script>
import TodoForm from "@/components/todo/TodoForm";

export default {
  el: '#todo-list',
  data: function () {
    return {
      todos: [
        {}
      ]
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