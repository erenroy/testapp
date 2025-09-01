<template>
  <section class="py-16 px-4 sm:px-6 lg:px-8 bg-white" ref="sectionRef">
    <div class="max-w-full mx-auto px-4">
      <!-- Section Header -->
      <div class="text-center mb-16" ref="headerRef">
        <div class="inline-block bg-accentlight rounded-full px-6 py-2 mb-6 transform transition-all duration-[1200ms] ease-out"
             :class="headerVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <span class="text-accent font-brand font-brand-medium text-sm">Our Special Solutions</span>
        </div>
        <h2 class="text-4xl md:text-5xl lg:text-6xl font-brand font-brand-bold text-text-primary mb-8 leading-tight transform transition-all duration-[1200ms] ease-out delay-200"
            :class="headerVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          We Customize Your Software to The
          <br class="hidden md:block">
          Smart Ways
        </h2>
      </div>

      <!-- Solutions Grid - 2 rows of 4 -->
      <div class="max-w-7xl mx-auto" ref="gridRef">
        <!-- First Row -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-8">
          <!-- Realtime Analytics -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '300ms' : '0ms' }">
            <!-- Background Decoration -->
            <div class="absolute top-4 left-4 w-16 h-8 opacity-10 group-hover:opacity-20 transition-opacity duration-200">
              <div class="flex space-x-1">
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
              </div>
              <div class="flex space-x-1 mt-1 ml-2">
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
                <div class="w-1 h-1 bg-accent group-hover:bg-white rounded-full transition-colors duration-200"></div>
              </div>
            </div>

            <!-- Icon -->
            <div class="mb-6 relative z-10 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
                  <circle cx="18" cy="8" r="3" stroke="currentColor" stroke-width="2" fill="none" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Realtime Analytics
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>

          <!-- Media Friendly -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '450ms' : '0ms' }">
            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 4V2a1 1 0 011-1h8a1 1 0 011 1v2M7 4h10M7 4v16a1 1 0 001 1h8a1 1 0 001-1V4M11 8h2M11 12h2M11 16h2" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Media Friendly
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>

          <!-- Fast and Intuitive -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '600ms' : '0ms' }">
            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <circle cx="12" cy="12" r="10" stroke="currentColor" stroke-width="2" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6l4 2" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Fast and Intuitive
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>

          <!-- Well Integrated -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg relative h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '750ms' : '0ms' }">
            <!-- Decorative Plus -->
            <div class="absolute top-6 right-6 text-accent group-hover:text-white opacity-20 transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z" />
              </svg>
            </div>

            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Well Integrated
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>
        </div>

        <!-- Second Row -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <!-- Cloud Storage -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '900ms' : '0ms' }">
            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Cloud Storage
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>

          <!-- Mobile Optimized -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '1050ms' : '0ms' }">
            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a1 1 0 001-1V4a1 1 0 00-1-1H8a1 1 0 00-1 1v16a1 1 0 001 1z" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Mobile Optimized
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>

          <!-- Secure Platform -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '1200ms' : '0ms' }">
            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              Secure Platform
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>

          <!-- 24/7 Support -->
          <div class="group bg-white hover:bg-accent rounded-2xl p-8 border border-border hover:shadow-xl shadow-lg h-80 flex flex-col cursor-pointer text-center transform scroll-transition card-hover-scale"
               :class="cardsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: cardsVisible ? '1350ms' : '0ms' }">
            <!-- Icon -->
            <div class="mb-6 flex justify-center">
              <div class="w-16 h-16 bg-accentlight group-hover:bg-white group-hover:bg-opacity-20 rounded-xl flex items-center justify-center transition-all duration-200 ease-in-out">
                <svg class="w-8 h-8 text-accent group-hover:text-white transition-colors duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192L5.636 18.364M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z" />
                </svg>
              </div>
            </div>

            <h3 class="text-xl font-brand font-brand-semibold text-text-primary group-hover:text-white mb-4 transition-colors duration-200 ease-in-out">
              24/7 Support
            </h3>
            
            <p class="text-text-secondary group-hover:text-white group-hover:text-opacity-90 font-brand leading-relaxed flex-grow transition-colors duration-200 ease-in-out">
              Sed ut perspiciatis unde omnis natus error voluptatem accusante dolorem laudantium totam aperiam eaque ipsa quae inventore
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// Animation state
const headerVisible = ref(false)
const cardsVisible = ref(false)
const sectionRef = ref(null)
const headerRef = ref(null)
const gridRef = ref(null)

// Scroll to top function
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}

// Intersection Observer for scroll animations
let headerObserver = null
let gridObserver = null

onMounted(() => {
  // Header animation observer
  headerObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          headerVisible.value = true
        }
      })
    },
    {
      threshold: 0.2,
      rootMargin: '0px'
    }
  )

  // Grid animation observer
  gridObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          cardsVisible.value = true
        }
      })
    },
    {
      threshold: 0.1,
      rootMargin: '0px'
    }
  )

  if (headerRef.value) {
    headerObserver.observe(headerRef.value)
  }

  if (gridRef.value) {
    gridObserver.observe(gridRef.value)
  }
})

onUnmounted(() => {
  if (headerObserver) {
    headerObserver.disconnect()
  }
  if (gridObserver) {
    gridObserver.disconnect()
  }
})
</script>

<style scoped>
/* Ensure smooth hardware acceleration */
.transform {
  transform: translateZ(0);
  will-change: transform, opacity;
}

/* Slow scroll animation - keeps original timing */
.scroll-transition {
  transition: opacity 1000ms cubic-bezier(0.25, 0.46, 0.45, 0.94),
              transform 1000ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

/* Fast hover scale - separate from scroll animation */
.card-hover-scale {
  /* This doesn't interfere with scroll transition */
}

.card-hover-scale:hover {
  transform: scale(1.05) translateY(0px) !important;
  z-index: 10;
  transition: transform 0.1s ease-out !important;
}

/* Ensure non-hovered cards maintain slow scroll transition */
.card-hover-scale:not(:hover) {
  transition: opacity 1000ms cubic-bezier(0.25, 0.46, 0.45, 0.94),
              transform 1000ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

/* Custom smooth easing curves */
.ease-out {
  transition-timing-function: cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.ease-in-out {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>
