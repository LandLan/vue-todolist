<template>
  <ul class="todo-list">
    <li v-for="item in itemData" v-bind:key="item.key">
      <TodoItem v-bind="item" v-on:deleteItem="handleDeleteItem"/>
    </li>
  </ul>
</template>

<script>
import TodoItem from './TodoItem'

export default {
  name: 'TodoList',
  components: {
    TodoItem
  },
  data () {
    return {
      itemData: this.itemlist
    }
  },
  props: [ 'itemlist' ],
  methods: {
    handleDeleteItem: function (num) {
      this.itemData.forEach((item, index) => {
        if (item.num === num) {
          this.itemData.splice(index, 1)
        }
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
