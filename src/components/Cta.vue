<template>
  <!-- CTA Section -->
  <section id="cta" class="relative py-24 bg-darkViolet">
    <!-- Background Image -->
    <img
      :src="backgroundImage"
      alt="Background"
      class="absolute inset-0 w-full h-full object-cover -z-10"
    />
    <div class="relative flex flex-col p-2 space-y-6">
      <h5
        class="mx-auto space-y-10 text-4xl font-bold text-center text-white"
      >
        {{ title }}
      </h5>
      <button
        class="px-10 py-5 mx-auto text-2xl font-bold text-white rounded-full bg-cyan hover:bg-cyanLight md:text-base md:py-3 focus:outline-none"
        @click="ctaAction"
      >
        {{ buttonText }}
      </button>
    </div>
  </section>
</template>

<script>
export default {
  name: "CTASection",
  props: {
    title: {
      type: String,
      default: "Boost your links today",
    },
    buttonText: {
      type: String,
      default: "Get Started",
    },
    backgroundImage: {
      type: String,
      default: require('@/assets/bgP.jpg'),
    },
  },
  methods: {
    ctaAction() {
      this.$emit("cta-click");
    },
  },
};
</script>

<style scoped>
/* Ensure the content layers above the background */
.relative {
  z-index: 1;
}
.absolute {
  z-index: -1;
}
</style>