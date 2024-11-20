<template>
  <div class="flex flex-col space-y-2 items-center justify-center ">
    <Task v-for="task in tasks" :key="task.id" :task="task" />
  </div>
</template>

<script>
import Task from './Task.vue';

export default {
  name: 'Tasks',
  props: {
    tasks: {
      type: Array,
      required: true,
    },
  },
  components: {
    Task,
  },
};
</script>