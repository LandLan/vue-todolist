<template>
  <div class="todo-container">
    <TodoInput v-on:addItem="addItem"/>
    <TodoList :itemlist="itemlist"/>
  </div>
</template>

<script>
import TodoInput from './TodoInput'
import TodoList from './TodoList'

export default {
  name: 'TodoContainer',
  components: {
    TodoInput,
    TodoList
  },
  data () {
    return {
      num: 0,
      itemlist: []
    }
  },
  methods: {
    addItem: function (name) {
      this.itemlist.push({ todo: name, num: this.num + 1 })
      this.num = this.num + 1
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
