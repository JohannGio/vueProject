<template>
  <div class="p-5 flex flex-col items-center justify-center mb-2 bg-red-50 w-[400px] rounded">
    <h3 class="text-lg font-bold">{{ task.text }}</h3>
    <p class="text-sm text-blue-500">{{ task.day }}</p>
  </div>
</template>

<script>
export default {
  name: 'Task',
  props: {
    task: {
      type: Object,
      required: true,
    },
  },
};
</script>