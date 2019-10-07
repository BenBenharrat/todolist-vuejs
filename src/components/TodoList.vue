<template>
  <div>
    <TodoListInputText v-model="newTodoText" />
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
    }
};
</script>

<style>

</style>