<template>
  <div class="container">
    <h1 class="container--header">Manage Your Task</h1>
    <div class="container--body">
      <div class="container--body__button">
        <nuxt-link to="/addtodo">
          <Button name="ToDoの追加" />
        </nuxt-link>
        <nuxt-link to="edittodo">
          <Button name="ToDoの編集" />
        </nuxt-link>
        <nuxt-link to="deletetodo">
          <Button name="ToDoの削除" />
        </nuxt-link>
      </div>
      <p>ここにリストを表示させる</p>
      <Form @addedTodo="newTodo" />
      <List :todos="todos" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        // {
        //   id: 1,
        //   title: "Task1"
        // },
        // {
        //   id: 2,
        //   title: "Task2"
        // },
        // {
        //   id: 3,
        //   title: "Task3"
        // },
        'task1'
      ]
    }
  },
  methods: {
    newTodo(todo) {
      this.todos.push(todo);
      console.log(todo)
      console.log(this.todos)
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  text-align: center;
  display: flex;
  flex-direction: column;
}

.container--header {
  padding: 20px;
}

.container--body__button {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

/* .title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
} */
</style>
