<template>
  <div class="todo-input">
    <input placeholder="Todo" v-on:keyup.enter="handleAddTodo($event)" />
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data () {
    return {}
  },
  methods: {
    handleAddTodo: function (event) {
      let todo = event.target.value
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
