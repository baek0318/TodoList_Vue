<template>
  <div id="bottom-bar">
    <input placeholder="할일을 입력해주세요" v-on:change="textHandler" v-on:keypress="textEnterHandler"/>
    <button v-on:click="clickHandler">등록</button>
  </div>
</template>

<script>
export default {
  el: '#bottom-bar',
  props: ['clickHandler', 'textHandler', 'textEnterHandler']
}
</script>

<style>
#bottom-bar {
  background-color: #1e2934;
}
</style>