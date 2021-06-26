<template>
  <li>
    <div id="todo-form">
      <input type="checkbox"/>
      <div>{{todoTitle}}</div>
    </div>
  </li>
</template>

<script>
export default {
  el : '#todo-form',
  data: function() {
    return {
      todoTitle: '오늘 할일을 입력해주세요'
    }
  }
}
</script>

<style>
#todo-form {
  background-color: #273645;
  display: flex;
}
</style>