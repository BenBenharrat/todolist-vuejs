<template>
  <div>
    <TodoListInputText v-model="newTodoText" @keydown.enter="addTodo"/>
    <TodoListItem :todos="todos" />
  </div>
</template>

<script>
import TodoListInputText from '@/components/TodoListInputText.vue';
import TodoListItem from '@/components/TodoListItem.vue';

export default {
    components: {
        TodoListInputText,
        TodoListItem
    },
    data() {
      return {
        newTodoText:"toto",
        todos: ["Tomato", "Milk", "Butter"]
      };
    },
    methods: {
      addTodo() {
        const trimmedText = this.newTodoText.trim();
        if(trimmedText) {
          this.todos.push(trimmedText);
          this.newTodoText = "";
        }
      }
    },
};
</script>

<style>

</style>