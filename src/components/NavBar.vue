<template>
  <!-- Nav Bar -->
  <nav class="relative container mx-auto p-6">
    <!-- Flex-Container for all items -->
    <div class="flex items-center justify-between">
      <!-- Flex container left -->
      <div class="flex items-center space-x-20">
        <!-- Logo -->
        <img src="@/assets/logo.png" class="w-[40px]" alt="Logo">
        <!-- Menu -->
        <div class="hidden space-x-8 font-bold lg:flex">
          <a href="#" class="text-grayishViolet hover:text-veryDarkViolet">Features</a>
          <a href="#" class="text-grayishViolet hover:text-veryDarkViolet">Pricing</a>
          <a href="#" class="text-grayishViolet hover:text-veryDarkViolet">Resources</a>
        </div>
      </div>
      <!-- Flex container right -->
      <div class="hidden lg:flex items-center space-x-6 font-bold text-grayishViolet">
        <div class="hover:text-veryDarkViolet">Login</div>
        <!-- Button -->
        <a href="#" class="px-8 py-3 font-bold text-white bg-cyan rounded-full hover:opacity-70">
          Sign Up
        </a>
      </div>
      <!-- Hamburger Menu -->
      <button
        @click="toggleMenu"
        id="menu-btn"
        class="block lg:hidden hamburguer focus:outline-none"
        type="button"
      >
        <span class="hamburguer-top"></span>
        <span class="hamburguer-middle"></span>
        <span class="hamburguer-bottom"></span>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="isMenuOpen"
      id="menu"
      class="absolute p-6 rounded-lg bg-darkViolet left-6 right-6 top-20 z-100"
    >
      <div class="flex flex-col items-center justify-center w-full space-y-6 font-bold text-white rounded-sm">
        <a href="#" class="w-full text-center">Features</a>
        <a href="#" class="w-full text-center">Pricing</a>
        <a href="#" class="w-full text-center">Resources</a>
        <a href="#" class="w-full text-center border-t pt-5 border-gray-400">Login</a>
        <a href="#" class="w-full text-center">Sign up</a>
        <a href="#" class="w-full text-center py-3 rounded-full bg-cyan">Features</a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style scoped>
/* Styles for the hamburger menu */
.hamburguer {
  cursor: pointer;
  width: 25px;
  height: 20px;
  position: relative;
}
.hamburguer span {
  background: #000;
  display: block;
  height: 3px;
  margin: 4px 0;
  transition: all 0.3s ease-in-out;
}
.hamburguer-top {
  transform-origin: top left;
}
.hamburguer-middle {
  opacity: 1;
}
.hamburguer-bottom {
  transform-origin: bottom left;
}
.hamburguer:hover span {
  background: #555;
}
</style>