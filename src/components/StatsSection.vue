<template>
  <!-- Stats Section -->
  <section id="stats" class="bg-gray-100 py-[50px]">
    <div class="container mx-auto px-3">
      <h2 class="text-4xl mb-6 font-bold text-center">{{ title }}</h2>
      <p class="max-w-xs mx-auto text-center text-gray-400 md:max-w-md">
        {{ description }}
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "StatsSection",
  props: {
    title: {
      type: String,
      default: "Advance Statistics",
    },
    description: {
      type: String,
      default:
        "Track how your links are performing across the web with our advance statistics dashboard.",
    },
  },
};
</script>

<style scoped>
/* Add any scoped styles if needed */
</style>