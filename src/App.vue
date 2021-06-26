<template>
  <div>
    <headerbar></headerbar>
    <todolist></todolist>
    <bottombar></bottombar>
  </div>
</template>

<script>
import BottomBar from './components/bottom/BottomBar';
import HeaderBar from './components/header/HeaderBar';
import TodoList from './components/todo/TodoList';

export default {
  components: {
    'bottombar': BottomBar,
    'headerbar': HeaderBar,
    'todolist': TodoList
  }
}

</script>

<style>

</style>