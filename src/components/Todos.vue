<template>
  <div>
    <h1>Todos</h1>
    <div>
      <div v-bind:key="todo.id" v-for="todo in todos">
        <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
      </div>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "Todos",
  components: { TodoItem },
  props: ["todos"],
  methods: {}
};
</script>

<style scoped>
</style>
