<template>
  <div style="margin:30px">
    <h1>todos</h1>
    <hr>
    <div>
      <input placeholder="动弹一下" @keyup.enter="addTodo">
      <button @click="remove">
        删除
      </button>
    </div>
    <ol>
      <li v-for="todo in list" :key="todo.text">
        <label>
          <input type="checkbox" :checked="todo.done" @change="toggle(todo)">
          <span :class="{ done: todo.done }">{{ todo.text }}</span>
        </label>
      </li>
    </ol>
  </div>
</template>

<script>
import { mapState, mapMutations } from 'vuex'
export default {
  name: 'Todos',
  components: {
    // HelloWorld
  },
  props: {},
  data () {
    return {}
  },
  computed: {
    // 映射 store.state
    ...mapState({
      list: state => state.todos.list
    })
  },
  methods: {
    addTodo (e) {
      this.add(e.target.value)
      e.target.value = ''
    },
    // 映射store.mutations
    ...mapMutations({
      add: 'todos/add',
      remove: 'todos/remove',
      toggle: 'todos/toggle'
    })
  }
}
</script>

<style>
  .done {
      text-decoration: line-through;
  }
</style>
