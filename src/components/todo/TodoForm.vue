<template>
  <li>
    <div id="todo-form">
      <input type="checkbox"/>
      <div>{{todo}}</div>
    </div>
  </li>
</template>

<script>
export default {
  el : '#todo-form',
  props: ['todoItem'],
  data: function() {
    return {
      todo: this.todoItem
    }
  }
}
</script>

<style>
#todo-form {
  background-color: #273645;
  display: flex;
}

#todo-form div {
  color: white;
}
</style>