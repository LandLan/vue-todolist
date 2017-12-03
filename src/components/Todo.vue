<template>
  <div>
    <div class="todo-input">
      <input ref="input" v-bind:value="todo" placeholder="Todo something"
          v-on:keyup.enter="handleAddTodo($event.target.value)" />
    </div>
    <ul class="todo-list">
      <li v-for="item in itemData" v-bind:key="item.key">
        {{ item.todo }}
        <button v-on:click="handleDeleteTodo(item.key)">删除</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todo',
  data () {
    return {
      itemData: [],
      num: 0
    }
  },
  props: [ 'todo' ],
  methods: {
    handleAddTodo: function (value) {
      this.itemData.push({todo: value, key: (this.num + 1)})
      this.num = this.num + 1
      this.$refs.input.todo = ''
    },
    handleDeleteTodo: function (key) {
      this.itemData.forEach((item, index) => {
        if (item.key === key) {
          this.itemData.splice(index, 1)
        }
      })
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
  padding: 0;
}
a {
  color: #42b983;
}
</style>
