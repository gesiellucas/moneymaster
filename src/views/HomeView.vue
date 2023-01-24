<template>
  <div>
    <form @submit.prevent="addTodo">
      <input v-model="newTodo" placeholder="Add a todo"/>
      <button>Add</button>
    </form>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
        <button @click="removeTodo(todo.id)">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodo: '',
      todos: [
        { id: 1, text: 'Learn Vue.js' },
        { id: 2, text: 'Build a todo app' },
      ]
    }
  },
  methods: {
    addTodo() {
      this.todos.push({
        id: this.todos.length + 1,
        text: this.newTodo
      });
      this.newTodo = '';
    },
    removeTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>
