<template>
  <!-- Gray overlay background -->
  <div 
    v-if="activeMenu" 
    class="fixed inset-0 bg-black bg-opacity-20 z-40"
    @click="closeMenu"
  ></div>

  <!-- Navbar -->
  <header class="w-full border-b border-border sticky top-0 bg-white z-40">
    <nav class="max-w-none mx-auto flex items-center justify-between px-16 py-3">
      <!-- Logo -->
      <div class="flex items-center">
        <img src="/images/logo.jpg" alt="Logo" class="h-14 w-auto">
      </div>

      <!-- Desktop Navigation -->
      <ul class="hidden md:flex items-center gap-2 text-navlink font-semibold" @mouseleave="clearActiveMenu">
        <!-- Home -->
        <li class="relative">
          <a 
            href="/" 
            class="flex items-center gap-1 py-2 px-4 rounded text-base hover:text-accent transition-all duration-300 border-b-2 border-transparent hover:border-accent cursor-pointer"
          >
            Home
          </a>
        </li>

        <!-- Platform -->
        <li class="relative">
          <a 
            href="#" 
            class="flex items-center gap-1 py-2 px-4 rounded text-base hover:text-accent transition-all duration-300 border-b-2 border-transparent hover:border-accent cursor-pointer"
            @mouseenter="setActiveMenu('platform')"
          >
            Platform
            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
            </svg>
          </a>
        </li>

        <!-- Devices -->
        <li class="relative">
          <a 
            href="#" 
            class="flex items-center gap-1 py-2 px-4 rounded text-base hover:text-accent transition-all duration-300 border-b-2 border-transparent hover:border-accent cursor-pointer"
            @mouseenter="setActiveMenu('devices')"
          >
            Devices
            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
            </svg>
          </a>
        </li>

        <!-- Store - Simple Link -->
        <li class="relative">
          <a 
            href="/pricing" 
            class="flex items-center gap-1 py-2 px-4 rounded text-base hover:text-accent transition-all duration-300 border-b-2 border-transparent hover:border-accent cursor-pointer"
          >
            Store
          </a>
        </li>

        <!-- Resources -->
        <li class="relative">
          <a 
            href="#" 
            class="flex items-center gap-1 py-2 px-4 rounded text-base hover:text-accent transition-all duration-300 border-b-2 border-transparent hover:border-accent cursor-pointer"
            @mouseenter="setActiveMenu('resources')"
          >
            Resources
            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
            </svg>
          </a>
        </li>

        <!-- Support -->
        <li class="relative">
          <a 
            href="#" 
            class="flex items-center gap-1 py-2 px-4 rounded text-base hover:text-accent transition-all duration-300 border-b-2 border-transparent hover:border-accent cursor-pointer"
            @mouseenter="setActiveMenu('support')"
          >
            Support
            <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
            </svg>
          </a>
        </li>
      </ul>

      <!-- Desktop Right section -->
      <div class="hidden md:flex items-center gap-3">
        
        <div class="border-r border-border h-6 mx-2"/>
        
        <!-- Login/Signup text -->
        <a href="https://cloud.stationpoint.io/" class="py-2 px-3 rounded hover:bg-accentlight transition-all duration-300 font-semibold text-navlink hover:text-accent">
          Login / Signup
        </a>
        
        <!-- Cloud button -->
        <a href="https://cloud.stationpoint.io/" class="ml-2 px-6 py-2 rounded-lg bg-accent hover:bg-accent text-white font-semibold shadow-lg hover:shadow-xl transition-all duration-300 text-base flex items-center gap-2">
          Get Started
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14m-7-7l7 7-7 7"/>
          </svg>
        </a>
      </div>

      <!-- Mobile hamburger menu -->
      <button class="md:hidden ml-2 relative z-50 p-2" @click="toggleMobileMenu" aria-label="Menu">
        <span :class="['block w-7 h-[2px] rounded-sm bg-navlink mb-[5px] transform transition-all duration-300', mobileOpen ? 'rotate-45 translate-y-[7px] bg-accent' : '']"></span>
        <span :class="['block w-7 h-[2px] rounded-sm bg-navlink mb-[5px] transition-all duration-300', mobileOpen ? 'opacity-0' : '']"></span>
        <span :class="['block w-7 h-[2px] rounded-sm bg-navlink transition-all duration-300', mobileOpen ? '-rotate-45 -translate-y-[7px] bg-accent' : '']"></span>
      </button>
    </nav>
  </header>

  <!-- Professional Mega Menu -->
  <transition name="mega-menu">
    <div 
      v-if="activeMenu" 
      class="fixed top-50 left-1/2 transform -translate-x-1/2 z-50 w-full max-w-6xl mx-auto px-4"
      @mouseenter="keepMenuOpen"
      @mouseleave="closeMenu"
    >
      <div class="bg-white rounded-xl shadow-xl border border-gray-200 overflow-hidden backdrop-blur-sm">
        
        <!-- Platform Menu -->
        <div v-if="activeMenu === 'platform'" class="p-8">
          <div class="text-center mb-8">
            <h2 class="text-3xl font-bold text-gray-900 mb-2">Platform</h2>
            <p class="text-gray-600">Comprehensive IoT solutions for your business</p>
          </div>
          <div class="grid grid-cols-2 gap-8">
            <div class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-blue-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-blue-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-blue-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M7 19h10a2 2 0 002-2V7a2 2 0 00-2-2H7a2 2 0 00-2 2v10a2 2 0 002 2zM9 9h6v6H9V9z"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">IoT Platform</h3>
                </div>
                <p class="text-gray-600">Comprehensive platform for device management and data analytics</p>
              </div>
            </div>
            <div class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-green-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-green-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-green-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">Cloud Services</h3>
                </div>
                <p class="text-gray-600">Scalable cloud infrastructure for your IoT applications</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Devices Menu - Single box taking full width -->
        <div v-if="activeMenu === 'devices'" class="p-8">
          <div class="text-center mb-8">
            <h2 class="text-3xl font-bold text-gray-900 mb-2">Devices</h2>
            <p class="text-gray-600">Advanced IoT hardware for every application</p>
          </div>
          <div class="grid grid-cols-1 gap-8">
            <a href="/platform" class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-purple-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-purple-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-purple-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">Station Point Pro</h3>
                </div>
                <p class="text-gray-600">Advanced sensing technology for comprehensive monitoring available on Amazon</p>
              </div>
            </a>
          </div>
        </div>

        <!-- Resources Menu -->
        <div v-if="activeMenu === 'resources'" class="p-8">
          <div class="text-center mb-8">
            <h2 class="text-3xl font-bold text-gray-900 mb-2">Resources</h2>
            <p class="text-gray-600">Learn, explore, and get the most out of our platform</p>
          </div>
          <div class="grid grid-cols-2 gap-8">
            <div class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-teal-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-teal-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-teal-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-teal-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">Documentation</h3>
                </div>
                <p class="text-gray-600">Comprehensive guides and technical documentation</p>
              </div>
            </div>
            <div class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-cyan-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-cyan-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-cyan-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-cyan-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">Learning Center</h3>
                </div>
                <p class="text-gray-600">Interactive tutorials and educational content</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Support Menu -->
        <div v-if="activeMenu === 'support'" class="p-8">
          <div class="text-center mb-8">
            <h2 class="text-3xl font-bold text-gray-900 mb-2">Support</h2>
            <p class="text-gray-600">Get help when you need it, whenever you need it</p>
          </div>
          <div class="grid grid-cols-2 gap-8">
            <div class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-rose-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-rose-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-rose-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-rose-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192L5.636 18.364M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">Help Center</h3>
                </div>
                <p class="text-gray-600">Find answers and get personalized assistance</p>
              </div>
            </div>
            <div class="group cursor-pointer">
              <div class="bg-white border border-gray-200 rounded-xl p-6 hover:shadow-lg hover:border-violet-300 transition-all duration-300">
                <div class="flex items-center mb-4">
                  <div class="w-12 h-12 bg-violet-100 rounded-lg flex items-center justify-center mr-4 group-hover:bg-violet-500 transition-all duration-200">
                    <svg class="w-6 h-6 text-violet-600 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
                    </svg>
                  </div>
                  <h3 class="text-xl font-bold text-gray-900">24/7 Support</h3>
                </div>
                <p class="text-gray-600">Round-the-clock assistance for critical issues</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>

  <!-- Mobile menu overlay -->
  <transition name="mobile-fade">
    <div v-if="mobileOpen" class="md:hidden fixed inset-0 z-40 bg-white overflow-auto">
      <div class="flex flex-col h-full justify-start items-center pt-20 pb-10 px-6">
        <div class="text-center space-y-8 w-full max-w-sm">
          <ul class="space-y-6 text-2xl font-semibold text-navlink">
            <li><a href="#" @click="closeMobileMenu" class="block py-3 hover:text-accent transition-all duration-300">Home</a></li>
            <li><a href="#" @click="closeMobileMenu" class="block py-3 hover:text-accent transition-all duration-300">Platform</a></li>
            <li><a href="#" @click="closeMobileMenu" class="block py-3 hover:text-accent transition-all duration-300">Devices</a></li>
            <li><a href="/pricing" @click="closeMobileMenu" class="block py-3 hover:text-accent transition-all duration-300">Store</a></li>
            <li><a href="#" @click="closeMobileMenu" class="block py-3 hover:text-accent transition-all duration-300">Resources</a></li>
            <li><a href="#" @click="closeMobileMenu" class="block py-3 hover:text-accent transition-all duration-300">Support</a></li>
          </ul>

          <div class="flex flex-col gap-4 pt-6">
            <a href="#" @click="closeMobileMenu" class="px-8 py-4 rounded-lg bg-blue-500 hover:bg-blue-600 text-white font-semibold shadow-lg transition-all duration-300 text-lg">
              Cloud
            </a>
            <a href="#" @click="closeMobileMenu" class="px-8 py-4 rounded-lg bg-accentlight hover:bg-[#ebe7fa] text-accent font-semibold transition-all duration-300 text-lg">
              Login/Signup
            </a>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script setup>
import { ref } from 'vue'

const mobileOpen = ref(false)
const activeMenu = ref(null)

const toggleMobileMenu = () => { 
  mobileOpen.value = !mobileOpen.value 
}

const closeMobileMenu = () => { 
  mobileOpen.value = false
}

const setActiveMenu = (menu) => {
  if (hoverTimeout) {
    clearTimeout(hoverTimeout)
    hoverTimeout = null
  }
  activeMenu.value = menu
}

let hoverTimeout = null

const clearActiveMenu = () => {
  hoverTimeout = setTimeout(() => {
    activeMenu.value = null
  }, 150)
}

const keepMenuOpen = () => {
  if (hoverTimeout) {
    clearTimeout(hoverTimeout)
    hoverTimeout = null
  }
}

const closeMenu = () => {
  activeMenu.value = null
}
</script>

<style scoped>
.mega-menu-enter-active,
.mega-menu-leave-active {
  transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
}

.mega-menu-enter-from,
.mega-menu-leave-to {
  opacity: 0;
  transform: translate(-50%, -20px) scale(0.95);
}

.mega-menu-enter-to,
.mega-menu-leave-from {
  opacity: 1;
  transform: translate(-50%, 0) scale(1);
}

.mobile-fade-enter-active,
.mobile-fade-leave-active {
  transition: opacity 0.3s ease;
}

.mobile-fade-enter-from,
.mobile-fade-leave-to {
  opacity: 0;
}
</style>
