<template>
  <TodoListInputText />
</template>

<script>
import TodoListInputText from '@/components/TodoListInputText.vue';

export default {
    components: {
        TodoListInputText,
    },
    data() {
      return {
        todos: ["Tomato", "Milk", "Butter"]
      }
    },
};
</script>

<style>

</style>