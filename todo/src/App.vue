<template>
  <div id="app">
    <AddTodo />
    <h1>Todos</h1>
    <Todos />
  </div>
</template>

<script>
import AddTodo from './components/AddTodo.vue';
import Todos from './components/Todos.vue';

export default {
  name: 'App',
  components: {
    AddTodo,
    Todos,
  },
  created() {
    this.$store.dispatch('getTodos');
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  padding: 1em 0 0;
}
</style>
