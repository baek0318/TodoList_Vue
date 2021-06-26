<template>
  <div id="header-bar">
    <h1>{{name}} TodoList</h1>
  </div>
</template>

<script>
export default {
  el: '#header-bar',
  data: function () {
    return {
      name: '백승화'
    }
  }
}
</script>

<style>
#header-bar {
  background-color: #41af79;
}
</style>