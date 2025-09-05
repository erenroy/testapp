<template>
  <div class="bg-primary font-brand py-16">
    <div class="max-w-7xl mx-auto px-6">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <div 
          ref="headerRef"
          class="transform transition-all duration-1000 opacity-0 translate-y-8"
          :class="{ 'opacity-100 translate-y-0': headerVisible }"
        >
          <div class="inline-flex items-center px-4 py-2 bg-accent/10 rounded-full mb-6">
            <span class="text-accent text-sm font-brand-semibold uppercase tracking-wider">What's Included</span>
          </div>
          <h2 class="text-4xl md:text-5xl font-brand-bold text-text-primary mb-6 leading-tight">
            Station Point Pro <span class="text-accent">Complete Package</span>
          </h2>
          <p class="text-xl text-text-secondary max-w-3xl mx-auto leading-relaxed">
            Everything you need for comprehensive monitoring and control
          </p>
        </div>
      </div>

      <!-- Features Grid -->
      <div class="space-y-8">
        <!-- First Row - 3 Cards -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <!-- AC Current Sensors -->
          <div 
            ref="card1Ref"
            class="transform transition-all duration-700 opacity-0 translate-y-12"
            :class="{ 'opacity-100 translate-y-0': card1Visible }"
            style="transition-delay: 100ms;"
          >
            <div class="group relative bg-primary rounded-3xl p-8 shadow-lg hover:shadow-2xl transition-all duration-500 border-2 border-border hover:border-accent hover:-translate-y-3 overflow-hidden">
              <!-- Decorative corner -->
              <div class="absolute top-0 right-0 w-24 h-24 bg-accent/5 rounded-bl-3xl"></div>
              
              <div class="relative z-10">
                <!-- Icon Container -->
                <div class="w-20 h-20 bg-gradient-to-br from-accent to-accent/80 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300 shadow-lg">
                  <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                  </svg>
                </div>
                
                <h3 class="text-2xl font-brand-bold text-text-primary mb-4 group-hover:text-accent transition-colors duration-300">AC Current Sensors</h3>
                <p class="text-text-secondary leading-relaxed text-lg mb-6">3x 100A AC True RMS Clip On Current Sensors with 1ft cords for precise electrical monitoring</p>
                
                <!-- Feature Badge -->
                <div class="inline-flex items-center px-4 py-2 bg-accent/10 text-accent text-sm font-brand-semibold rounded-full border border-accent/20">
                  ⚡ True RMS Technology
                </div>
              </div>
            </div>
          </div>

          <!-- Submersible Level Sensor -->
          <div 
            ref="card2Ref"
            class="transform transition-all duration-700 opacity-0 translate-y-12"
            :class="{ 'opacity-100 translate-y-0': card2Visible }"
            style="transition-delay: 200ms;"
          >
            <div class="group relative bg-primary rounded-3xl p-8 shadow-lg hover:shadow-2xl transition-all duration-500 border-2 border-border hover:border-accent hover:-translate-y-3 overflow-hidden">
              <!-- Decorative corner -->
              <div class="absolute top-0 right-0 w-24 h-24 bg-accent/5 rounded-bl-3xl"></div>
              
              <div class="relative z-10">
                <!-- Icon Container -->
                <div class="w-20 h-20 bg-gradient-to-br from-accent to-accent/80 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300 shadow-lg">
                  <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"></path>
                  </svg>
                </div>
                
                <h3 class="text-2xl font-brand-bold text-text-primary mb-4 group-hover:text-accent transition-colors duration-300">Submersible Level Sensor</h3>
                <p class="text-text-secondary leading-relaxed text-lg mb-6">0-5M certified accurate stainless steel caged sensor with 50ft cord for reliable depth monitoring</p>
                
                <!-- Feature Badge -->
                <div class="inline-flex items-center px-4 py-2 bg-accent/10 text-accent text-sm font-brand-semibold rounded-full border border-accent/20">
                  🌊 Waterproof Design
                </div>
              </div>
            </div>
          </div>

          <!-- Line Pressure Sensor -->
          <div 
            ref="card3Ref"
            class="transform transition-all duration-700 opacity-0 translate-y-12"
            :class="{ 'opacity-100 translate-y-0': card3Visible }"
            style="transition-delay: 300ms;"
          >
            <div class="group relative bg-primary rounded-3xl p-8 shadow-lg hover:shadow-2xl transition-all duration-500 border-2 border-border hover:border-accent hover:-translate-y-3 overflow-hidden">
              <!-- Decorative corner -->
              <div class="absolute top-0 right-0 w-24 h-24 bg-accent/5 rounded-bl-3xl"></div>
              
              <div class="relative z-10">
                <!-- Icon Container -->
                <div class="w-20 h-20 bg-gradient-to-br from-accent to-accent/80 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300 shadow-lg">
                  <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v4a2 2 0 01-2 2h-2a2 2 0 00-2-2z"></path>
                  </svg>
                </div>
                
                <h3 class="text-2xl font-brand-bold text-text-primary mb-4 group-hover:text-accent transition-colors duration-300">Line Pressure Sensor</h3>
                <p class="text-text-secondary leading-relaxed text-lg mb-6">500 PSI certified accurate pressure sensor with 1/4 NPT fitting and 30ft cord for system monitoring</p>
                
                <!-- Feature Badge -->
                <div class="inline-flex items-center px-4 py-2 bg-accent/10 text-accent text-sm font-brand-semibold rounded-full border border-accent/20">
                  📊 High Precision
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Second Row - 2 Centered Cards -->
        <div class="flex justify-center">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl w-full">
            <!-- Panel and Lid Security Sensors -->
            <div 
              ref="card4Ref"
              class="transform transition-all duration-700 opacity-0 translate-y-12"
              :class="{ 'opacity-100 translate-y-0': card4Visible }"
              style="transition-delay: 400ms;"
            >
              <div class="group relative bg-primary rounded-3xl p-8 shadow-lg hover:shadow-2xl transition-all duration-500 border-2 border-border hover:border-accent hover:-translate-y-3 overflow-hidden">
                <!-- Decorative corner -->
                <div class="absolute top-0 right-0 w-24 h-24 bg-accent/5 rounded-bl-3xl"></div>
                
                <div class="relative z-10">
                  <!-- Icon Container -->
                  <div class="w-20 h-20 bg-gradient-to-br from-accent to-accent/80 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300 shadow-lg">
                    <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path>
                    </svg>
                  </div>
                  
                  <h3 class="text-2xl font-brand-bold text-text-primary mb-4 group-hover:text-accent transition-colors duration-300">Security Sensors</h3>
                  <p class="text-text-secondary leading-relaxed text-lg mb-6">2x magnetic door sensors with ABS plastic housing, 3ft and 15ft cords, plus 3M adhesive mounting</p>
                  
                  <!-- Feature Badge -->
                  <div class="inline-flex items-center px-4 py-2 bg-accent/10 text-accent text-sm font-brand-semibold rounded-full border border-accent/20">
                    🔒 Tamper Detection
                  </div>
                </div>
              </div>
            </div>

            <!-- Cellular Antenna Kit -->
            <div 
              ref="card5Ref"
              class="transform transition-all duration-700 opacity-0 translate-y-12"
              :class="{ 'opacity-100 translate-y-0': card5Visible }"
              style="transition-delay: 500ms;"
            >
              <div class="group relative bg-primary rounded-3xl p-8 shadow-lg hover:shadow-2xl transition-all duration-500 border-2 border-border hover:border-accent hover:-translate-y-3 overflow-hidden">
                <!-- Decorative corner -->
                <div class="absolute top-0 right-0 w-24 h-24 bg-accent/5 rounded-bl-3xl"></div>
                
                <div class="relative z-10">
                  <!-- Icon Container -->
                  <div class="w-20 h-20 bg-gradient-to-br from-accent to-accent/80 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-3 transition-all duration-300 shadow-lg">
                    <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M8.111 16.404a5.5 5.5 0 017.778 0M12 20h.01m-7.08-7.071c3.904-3.905 10.236-3.905 14.141 0M1.394 9.393c5.857-5.857 15.355-5.857 21.213 0"></path>
                    </svg>
                  </div>
                  
                  <h3 class="text-2xl font-brand-bold text-text-primary mb-4 group-hover:text-accent transition-colors duration-300">Cellular Antenna Kit</h3>
                  <p class="text-text-secondary leading-relaxed text-lg mb-6">Omnidirectional LTE antenna with professional mounting bracket assembly and 15ft cord for reliable connectivity</p>
                  
                  <!-- Feature Badge -->
                  <div class="inline-flex items-center px-4 py-2 bg-accent/10 text-accent text-sm font-brand-semibold rounded-full border border-accent/20">
                    📡 LTE Connectivity
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// Refs for elements and visibility states
const headerRef = ref(null)
const card1Ref = ref(null)
const card2Ref = ref(null)
const card3Ref = ref(null)
const card4Ref = ref(null)
const card5Ref = ref(null)

const headerVisible = ref(false)
const card1Visible = ref(false)
const card2Visible = ref(false)
const card3Visible = ref(false)
const card4Visible = ref(false)
const card5Visible = ref(false)

// Intersection Observer for scroll animations
let observer

const observerOptions = {
  threshold: 0.1,
  rootMargin: '0px 0px -50px 0px'
}

const observerCallback = (entries) => {
  entries.forEach((entry) => {
    if (entry.isIntersecting) {
      if (entry.target === headerRef.value) headerVisible.value = true
      if (entry.target === card1Ref.value) card1Visible.value = true
      if (entry.target === card2Ref.value) card2Visible.value = true
      if (entry.target === card3Ref.value) card3Visible.value = true
      if (entry.target === card4Ref.value) card4Visible.value = true
      if (entry.target === card5Ref.value) card5Visible.value = true
    }
  })
}

onMounted(() => {
  observer = new IntersectionObserver(observerCallback, observerOptions)
  
  if (headerRef.value) observer.observe(headerRef.value)
  if (card1Ref.value) observer.observe(card1Ref.value)
  if (card2Ref.value) observer.observe(card2Ref.value)
  if (card3Ref.value) observer.observe(card3Ref.value)
  if (card4Ref.value) observer.observe(card4Ref.value)
  if (card5Ref.value) observer.observe(card5Ref.value)
})

onUnmounted(() => {
  if (observer) {
    observer.disconnect()
  }
})
</script>
