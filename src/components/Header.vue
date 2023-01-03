<template>
  <header>
    <h1>{{ title }}</h1>
  </header>
  <ButtonVue text="Add Task" color="Green" />
</template>

<script>
import ButtonVue from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: String,
  },
  components: {
    ButtonVue,
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
