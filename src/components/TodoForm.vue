<template>
  <div class="mb-4">
    <h1>Vue 3</h1>
    <h2>TypeScript Demo {{ version }}</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import { TodoType } from "@/models/todoModel";
import { v4 as uuidv4 } from "uuid";

export default defineComponent({
  name: "TodoForm",
  setup() {
    // local state
    const version = ref("v1");
    const newTodo = ref("");

    const todos = ref<TodoType[]>([]);

    function addNewTodo(): void {
      if (!newTodo.value) return;

      todos.value.push({
        id: uuidv4(),
        done: false,
        content: newTodo.value,
      });

      console.log("newTodo:", newTodo.value);

      newTodo.value = "";
    }

    return { version };
  },
});
</script>
