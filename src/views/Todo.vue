<template>
    <div>
        <h1> Todo List</h1>
        <ul>
          <input v-model="newTask">
          <button @click="addTask">ADD</button>
          <li v-for="todo in todos">
          {{todo}}
          </li>
        </ul>
    </div>

</template>
<script>
export default {
  data: function() {
    return ({
      newTask: "",
      todos: ["first task", "second task"]
    })
  },
  methods:{
    addTask() {
      this.todos.push(this.newTask)
    }
  }
};
</script>


