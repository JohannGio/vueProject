<template>
  <!-- Feature Box -->
  <div
    class="relative flex flex-col p-6 space-y-6 bg-white rounded-lg md:w-1/3"
    :class="customMt"
  >
    <!-- Image Positioning -->
    <div class="absolute -ml-10 -top-10 md:left-16 left-1/2">
      <!-- Image Container -->
      <div
        class="flex items-center justify-center w-20 h-20 p-4 rounded-full bg-veryDarkViolet"
      >
      <img src="@/assets/logo.png" class="w-[40px]" alt="Logo">
      </div>
    </div>
    <!-- Title -->
    <h5 class="pt-6 text-xl font-bold text-center capitalize md:text-left">
      {{ title }}
    </h5>
    <!-- Description -->
    <p class="text-center text-gray-400 md:text-left">
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  name: "FeatureBox",
  props: {
    imageSrc: {
      type: String,
      required: false,
    },
    title: {
      type: String,
      required: false,
    },
    description: {
      type: String,
      required: false,
    },
    customMt: {
      type: String,
      default: "mt-0",
    },
  },
};
</script>

<style scoped>
/* Add scoped styles if necessary */
</style>