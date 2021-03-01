<template>
  <div class="form">
    <form @submit.prevent="addTodo">
      <label>To Do</label>
      <input v-model="todo">
      <button type="submit">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todo: ''
    }
  },
  methods: {
    addTodo() {
      this.$emit('addedTodo', this.todo.title);
      this.todo = '';
    }
  }
}
</script>
