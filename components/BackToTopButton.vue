<!-- BackToTopButton.vue -->
<template>
    <button
      @click="scrollToTop"
      class="fixed bottom-4 right-4 p-3 bg-blue-500 text-white rounded-full shadow-md transition duration-300 hover:bg-blue-600"
      v-show="showButton"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        class="h-6 w-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M5 10l7-7m0 0l7 7m-7-7v18"
        />
      </svg>
    </button>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showButton: false,
      };
    },
    methods: {
      scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
      },
      handleScroll() {
        this.showButton = window.scrollY > 300;
      },
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    beforeDestroy() {
      window.removeEventListener('scroll', this.handleScroll);
    },
  };
  </script>
  
  <style scoped>
  
  /* Ajoutez vos styles personnalisés ici si nécessaire */
  </style>
  