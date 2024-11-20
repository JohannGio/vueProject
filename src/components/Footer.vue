<template>
  <!-- Footer -->
  <footer class="py-16 bg-veryDarkBlue">
    <div
      class="container mx-auto flex flex-col items-center justify-between space-y-16 md:flex-row md:space-y-0 md:items-start"
    >
      <!-- Logo -->
      <img src="@/assets/logo.png" class="w-[40px] mr-20" alt="Logo">

      <!-- Menu Container -->
      <div class="flex flex-col w-full md:flex-row md:space-x-8">
        <!-- Menus -->
        <div
          v-for="(menu, index) in menus"
          :key="index"
          class="flex flex-col items-center w-full md:items-start"
        >
          <div class="mb-5 font-bold text-white capitalize">{{ menu.title }}</div>
          <div class="flex flex-col items-center space-y-3 md:items-start">
            <a
              v-for="(link, linkIndex) in menu.links"
              :key="linkIndex"
              :href="link.href"
              class="capitalize text-grayishViolet hover:text-cyan"
            >
              {{ link.text }}
            </a>
          </div>
        </div>
      </div>

      <!-- Social Container -->
      <div class="flex space-x-6">
        <a
          v-for="(icon, iconIndex) in socialIcons"
          :key="iconIndex"
          :href="icon.href"
        >
        <img src="@/assets/logo.png" class="w-[20px]" alt="Logo">
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    logoSrc: {
      type: String,
      default: "@/assets/logo.svg",
    },
    menus: {
      type: Array,
      default: () => [
        {
          title: "Features",
          links: [
            { text: "Link Shortening", href: "#" },
            { text: "Branded Links", href: "#" },
            { text: "Analytics", href: "#" },
          ],
        },
        {
          title: "Blog",
          links: [
            { text: "Blog", href: "#" },
            { text: "About Us", href: "#" },
            { text: "Contact Us", href: "#" },
          ],
        },
        {
          title: "Company",
          links: [
            { text: "Career", href: "#" },
            { text: "Our Team", href: "#" },
            { text: "Contacts", href: "#" },
          ],
        },
      ],
    },
    socialIcons: {
      type: Array,
      default: () => [
        {
          src: "@/assets/logo.png",
          href: "#",
          alt: "Facebook",
        },
        {
          src: "@/assets/logo.png",
          href: "#",
          alt: "Twitter",
        },
        {
          src: "@/assets/logo.png",
          href: "#",
          alt: "Pinterest",
        },
        {
          src: "@/assets/logo.png",
          href: "#",
          alt: "Instagram",
        },
      ],
    },
  },
};
</script>

<style scoped>
/* Add scoped styles if necessary */
.ficon {
  width: 24px;
  height: 24px;
}
</style>