<template>
  <div class="list">
    <!-- <ul class="list--top">
      v-forでまわす
      <li class="list--top__content">{{ title }}</li>
    </ul> -->
    <ListItem v-for="todo in todos" :key="todo.id">{{ todo.id }}. Title{{ todo.title }}</ListItem>
    <div>{{ count }}</div>
    <button @click="counter">Add</button>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    todos: Array
  },
  data() {
    return {
      count: 10
    }
  },
  methods: {
    counter() {
      this.count += 1
    }
  }
}
</script>

<style>
.list--top {
  list-style: none;
  padding: 0;
}

.list--top__content {
  background: #ddd;
  margin-bottom: 20px;
  height: 40px;
  margin-right: 200px;
  margin-left: 200px;
  padding: 10px;
}
</style>
