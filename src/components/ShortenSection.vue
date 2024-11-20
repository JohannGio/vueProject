<template>
  <!-- Shorten Section -->
  <section id="shorten" class="relative bg-gray-100">
    <!-- Shorten Container -->
    <div class="max-w-4xl mx-auto p-6 space-y-6">
      <!-- Form -->
      <form
        id="link-form"
        class="link-form relative flex flex-col w-full p-10 -mt-20 space-y-4 bg-darkViolet rounded-lg md:flex-row md:space-y-0 md:space-x-3"
        @submit.prevent="shortenLink"
      >
        <input
          v-model="inputLink"
          type="url"
          class="flex flex-1 p-3 border-2 rounded-lg placeholder-yellow-500 focus:outline-orange"
          placeholder="Shorten a link here"
          id="link-input"
        />
        <button
          type="submit"
          class="px-10 py-3 text-white bg-cyan rounded-lg hover:bg-cyanLight focus:outline-none md:py-2"
        >
          Short it
        </button>
        <!-- Error message -->
        <div
          id="err-msg"
          v-if="errorMessage"
          class="absolute left-7 bottom-3 text-red text-sm italic"
        >
          {{ errorMessage }}
        </div>
      </form>

      <!-- Links -->
      <div
        v-for="(link, index) in links"
        :key="index"
        class="flex flex-col items-center justify-between w-full p-6 bg-white rounded-lg md:flex-row"
      >
        <p class="font-bold text-center text-veryDarkViolet md:text-left">
          {{ link.original }}
        </p>
        <!-- Right Container -->
        <div
          class="flex md:flex-row flex-col mt-3 md:mt-0 justify-between items-center space-x-5"
        >
          <p class="font-bold text-center text-cyan md:text-left">
            {{ link.shortened }}
          </p>
          <button
            @click="copyToClipboard(link.shortened)"
            class="px-10 py-3 text-white bg-cyan rounded-lg hover:bg-cyanLight focus:outline-none"
          >
            Copy
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ShortenSection",
  data() {
    return {
      inputLink: "",
      links: [
        {
          original: "http://frontmentor.io/org/ideas-for-frontend",
          shortened: "http://frontmentor.io",
        },
        {
          original: "http://frontmentor.io/org/design-tips",
          shortened: "http://frontmentor.io/design",
        },
      ],
      errorMessage: "",
    };
  },
  methods: {
    shortenLink() {
      if (!this.inputLink) {
        this.errorMessage = "Please add a link!";
        return;
      }
      this.errorMessage = "";
      const newLink = {
        original: this.inputLink,
        shortened: `http://short.ly/${Math.random().toString(36).substring(7)}`,
      };
      this.links.push(newLink);
      this.inputLink = "";
    },
    copyToClipboard(link) {
      navigator.clipboard.writeText(link).then(() => {
        alert("Copied to clipboard!");
      });
    },
  },
};
</script>

<style scoped>
/* Add any scoped styles if necessary */
</style>