<template>
  <div class="list">
    <ListItem v-for="todo in todos" :key="todo">{{ todo }}</ListItem>
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

    }
  },
  methods: {

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
