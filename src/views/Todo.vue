<template>
    <div>
        <h1> Todo List</h1>
        <ul>
          <input v-model="newTask">
          <button @click="addTask">ADD</button>
          <TodoItem v-for="todo in todos" :item="todo">
            {{todo.id}}
          </TodoItem>
        </ul>
    </div>

</template>
<script>
import TodoItem from "@/components/TodoItem.vue";

export default {
  data: function() {
    return {
      newTask: "",
      todos: [
        { id: 1, task: "first task", done: true },
        { id: 2, task: "second task", done: false }
      ]
    };
  },
  methods: {
    addTask() {
      this.todos.push(this.newTask);
    }
  },
  components: { TodoItem }
};
</script>


