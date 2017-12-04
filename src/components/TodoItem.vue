<template>
  <div class="todo-item">
      {{ todo }}
      <button v-on:click="handleDeleteTodo(num)">删除</button>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  methods: {
    handleDeleteTodo: function (num) {
      this.$emit('deleteItem', num)
    }
  },
  props: ['todo', 'num']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
