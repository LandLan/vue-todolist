<template>
  <div class="todo-input">
    <input ref="input" placeholder="Todo" v-on:keyup.enter="handleAddTodo($event.target.value)" />
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data () {
    return {}
  },
  methods: {
    handleAddTodo: function (value) {
      this.$refs.input.value = ''
      this.$emit('addItem', value)
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
