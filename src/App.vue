<template>
  <div class="container">
    <img alt="Vue logo" src="./assets/logo.png" />
    <TodoForm />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TodoForm from "./components/TodoForm.vue";

export default defineComponent({
  name: "App",
  components: {
    TodoForm,
  },
});
</script>

<style>
@import "../node_modules/bootstrap/dist/css/bootstrap.css";
</style>
