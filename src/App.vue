<template>
  <div id="container">
    <headerbar></headerbar>
    <todolist v-bind:items="todos"></todolist>
    <bottombar
        v-bind:click-handler="enter"
        v-bind:text-handler="textHandler"
        v-bind:text-enter-handler="textEnterHandler"
    >
    </bottombar>
  </div>
</template>

<script>
import BottomBar from './components/bottom/BottomBar';
import HeaderBar from './components/header/HeaderBar';
import TodoList from './components/todo/TodoList';

export default {
  el: '#container',
  data: function() {
    return {
      todos: [],
      todo : ""
    }
  },
  components: {
    'bottombar': BottomBar,
    'headerbar': HeaderBar,
    'todolist': TodoList
  },
  methods: {
    enter: function() {
      this.todos.push({text :this.todo});
      this.todo = ""
    },
    textHandler: function(event) {
      this.todo = event.target.value;
      event.target.value = "";
    },
    textEnterHandler: function(event) {
      if(event.keyCode === 13) {
        this.todos.push({text : event.target.value});
        event.target.value = "";
      }
    }
  }
}

</script>

<style>

</style>