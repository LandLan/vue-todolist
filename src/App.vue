<template>
  <div id="app">
    <div class="left">
      <Todo/>
    </div>
    <div class="right">
      <TodoContainer />
    </div>
  </div>
</template>

<script>
import Todo from './components/Todo'
import TodoContainer from './components/TodoContainer'

export default {
  name: 'app',
  components: {
    Todo,
    TodoContainer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.left, .right {
  width: 50%;
  float: left;
}
</style>
