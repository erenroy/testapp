<template>
  <div class="min-h-screen bg-primary font-brand text-[color:var(--text-primary)]">
    <!-- Top Welcome Banner -->
    <div class="bg-accent py-3 px-4 text-white text-center relative overflow-hidden">
      <!-- Decorative elements -->
      <div class="absolute left-4 top-1/2 transform -translate-y-1/2">
        <div class="flex gap-1">
          <div class="w-2 h-2 bg-white/30 rotate-45"></div>
          <div class="w-2 h-2 bg-white/30 rotate-45"></div>
          <div class="w-2 h-2 bg-white/30 rotate-45"></div>
        </div>
      </div>
      <div class="absolute right-4 top-1/2 transform -translate-y-1/2">
        <svg class="w-6 h-6 text-white/30" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
        </svg>
      </div>
      <h1 class="font-brand-semibold text-lg">Welcome to Station Point Site</h1>
    </div>

    <Navbar />

    <!-- This renders the current page -->
    <NuxtPage />

    <FloatingShapes />
    <Footer />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Footer from '../components/Footer.vue'
import FloatingShapes from '../components/FloatingShapes.vue'
import Navbar from '../components/Navbar.vue'
</script>

<style scoped>
/* Single smooth page animation */
.page-container {
  opacity: 0;
  transform: translateY(30px);
  animation: smoothPageLoad 1.2s ease-out 0.3s forwards;
}

@keyframes smoothPageLoad {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Mobile menu animation */
.mobile-fade-enter-active,
.mobile-fade-leave-active {
  transition: all 0.4s cubic-bezier(0.33, 0, 0.67, 1);
}
.mobile-fade-enter-from,
.mobile-fade-leave-to {
  opacity: 0;
  transform: scale(0.98) translateY(20px);
}

/* Mobile dropdown slide animation */
.dropdown-slide-enter-active,
.dropdown-slide-leave-active {
  transition: all 0.3s ease-out;
}
.dropdown-slide-enter-from,
.dropdown-slide-leave-to {
  opacity: 0;
  transform: translateY(-10px);
  max-height: 0;
}
.dropdown-slide-enter-to,
.dropdown-slide-leave-from {
  opacity: 1;
  transform: translateY(0);
  max-height: 300px;
}
</style>
