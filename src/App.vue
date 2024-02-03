<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style>
html, body{
  overflow-x: hidden !important;
  width: 100vw;
  max-width: 100vw !important;
  scroll-behavior: smooth;

}


</style>

<script>
export default {
  data() {
    return {
      // Debounce timer
      debounceTimer: null,
    };
  },
  mounted() {
    window.addEventListener('scroll', this.debouncedScrollHandler);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.debouncedScrollHandler);
    clearTimeout(this.debounceTimer); // Clear the debounce timer
  },
  methods: {
    debouncedScrollHandler() {
      clearTimeout(this.debounceTimer);
      this.debounceTimer = setTimeout(this.preventHorizontalScroll, 50);
    },
    preventHorizontalScroll() {
      const scrollLeft = window.pageXOffset || document.documentElement.scrollLeft;
      if (scrollLeft !== 0) {
        window.scrollTo(0, window.pageYOffset);
      }
    },
  },
};
</script>
