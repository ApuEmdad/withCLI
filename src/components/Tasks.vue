<template>
  <div :key="task.id" v-for="task in tasks" class="task">
    <!--capturing and  directly emitting the id -->
    <Task @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>

<script>
import Task from "./Task.vue";

export default {
  name: "Tasks",
  components: {
    Task,
  },
  props: {
    tasks: {
      type: Array,
      required: true,
    },
  },
  methods: {
    onDelete(id) {
      console.log(id);
    },
  },
  created() {
    console.log(this.tasks);
  },
  emits: ["delete-task"],
};
</script>

<style scope></style>
$
