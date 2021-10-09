<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @toggleform="$emit('toggleform')"
      :text="showFormTask ? 'Close' : 'Add Task'"
      :color="showFormTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  props: {
    title: String,
    showFormTask: Boolean,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
