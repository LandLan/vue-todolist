<template>
  <ul class="todo-list">
    <li>{{todoItem}}</li>
  </ul>
</template>

<script>
export default {
  name: 'TodoList',
  data () {
    return {}
  },
  methods: {
  },
  props: {
    todoItem: {
      type: String,
      default: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
