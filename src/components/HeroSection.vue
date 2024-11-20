<template>
  <!-- Hero Section -->
  <section id="hero" class="bg-gradient-to-r from-blue-100 to-green-100">
    <!-- Hero Main Container -->
    <div class="container flex flex-col-reverse mx-auto p-6 lg:flex-row">
      <!-- Left Container -->
      <div class="flex flex-col space-y-10 mb-44 lg:mt-16 lg:w-1/2 xl:mb-52">
        <h1
          class="text-5xl font-bold text-center lg:text-6xl lg:max-w-md lg:text-left"
        >
          {{ title }}
        </h1>
        <p
          class="text-2xl text-center text-gray-400 lg:max-w-md lg:text-left"
        >
          {{ description }}
        </p>
        <div class="mx-auto lg:mx-0">
          <a
            href="#"
            class="py-5 px-10 text-2xl font-bold text-white bg-cyan rounded-full lg:py-4 hover:opacity-70"
          >
            {{ buttonText }}
          </a>
        </div>
      </div>

      <!-- Image -->
      <div class="mb-24 mx-auto md:w-180 lg:mb-0 lg:w-1/2">
        <img src="@/assets/work.png" class="w-[800px]" alt="Logo">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
  props: {
    title: {
      type: String,
      default: 'More than just shorter links',
    },
    description: {
      type: String,
      default:
        "Build your brand's recognition and get detailed insights on how your links are performing.",
    },
    buttonText: {
      type: String,
      default: 'Get Started',
    },
    imageSrc: {
      type: String,
      default: '@/assets/working.jpg',
    },
    imageAlt: {
      type: String,
      default: 'Illustration of working',
    },
  },
};
</script>

<style scoped>
/* Add any scoped styles if needed */
</style>