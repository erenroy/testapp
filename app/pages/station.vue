<template>
  <div class="min-h-screen bg-white font-brand page-container" :class="{ 'page-loaded': pageLoaded }" ref="pageContainer">
    
    <!-- Top Purple Header Banner - MORE ANIMATED CIRCLES -->
    <section class="bg-accent text-white py-24 px-4 sm:px-6 lg:px-8 relative overflow-hidden animated-section" ref="headerSection">
      
      <!-- Enhanced Animated Decorative Elements -->
      
      <!-- More animated dotted grid pattern (top left) -->
      <div class="absolute top-12 left-16 animate-float-enhanced">
        <div class="grid grid-cols-6 gap-1">
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
        </div>
      </div>

      <!-- More animated plus sign (center) -->
      <div class="absolute top-8 left-1/2 transform -translate-x-1/2 text-4xl text-cyan-400 font-light animate-float-enhanced-delayed">+</div>

      <!-- More animated diamond grid pattern (center right) -->
      <div class="absolute top-16 right-1/3 animate-float-enhanced-slow">
        <div class="grid grid-cols-4 gap-1 transform rotate-45">
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
          <div class="w-1 h-1 bg-cyan-400 rounded-full"></div>
        </div>
      </div>

      <!-- More animated striped circle (top right) -->
      <div class="absolute top-8 right-20 w-32 h-32 animate-float-enhanced-bounce">
        <div class="w-full h-full rounded-full opacity-60" style="background: repeating-linear-gradient(45deg, transparent, transparent 3px, rgba(34, 211, 238, 0.4) 3px, rgba(34, 211, 238, 0.4) 6px);"></div>
      </div>

      <!-- Main Content -->
      <div class="max-w-7xl mx-auto relative z-10 slide-in-left">
        <h1 class="text-5xl md:text-6xl font-brand-bold text-white mb-4">Station List Pro</h1>
        <nav class="flex items-center space-x-2 text-lg text-purple-200">
          <a href="/" class="hover:text-white transition-colors duration-200">Home</a>
          <span class="text-white/60">›</span>
          <span class="text-white font-brand-semibold underline">Project Details</span>
          <!-- Small triangle after breadcrumb -->
          <div class="ml-2 w-0 h-0 border-l-4 border-r-4 border-t-4 border-l-transparent border-r-transparent border-t-white/60"></div>
        </nav>
      </div>
    </section>

    <!-- Main Project Content -->
    <section class="py-12 mx-[5%] animated-section" ref="mainSection">
      <div class="w-full">
        <div class="relative">
          
          <!-- Large Hero Image with Purple Sidebar -->
          <div class="relative mb-16 scroll-fade-in" ref="heroImageSection">
            <div class="w-full h-[500px] bg-gray-200 overflow-hidden slide-in-up">
              <img 
                src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=1400&q=80" 
                alt="Station Point Pro Dashboard Interface" 
                class="w-full h-full object-cover"
              />
            </div>
            
            <!-- Project Info Sidebar -->
            <div class="absolute top-[70%] right-8 bg-accent rounded-lg p-8 text-white shadow-xl w-96 h-[540px] z-10 slide-in-right">
              <h3 class="text-2xl font-brand-bold mb-6 text-left">Project Info</h3>
              <div class="w-full border-t-4 border-white opacity-80 mb-8"></div>
              
              <div class="space-y-6 text-left">
                <div class="fade-in-item" style="animation-delay: 0.2s">
                  <p class="text-purple-200 font-brand-medium mb-2 text-sm">Category</p>
                  <p class="font-brand-semibold text-xl">Web Design</p>
                  <div class="w-full border-t border-white opacity-40 mt-4"></div>
                </div>
                
                <div class="fade-in-item" style="animation-delay: 0.4s">
                  <p class="text-purple-200 font-brand-medium mb-2 text-sm">Client</p>
                  <p class="font-brand-semibold text-xl">Jonathan D. Silva</p>
                  <div class="w-full border-t border-white opacity-40 mt-4"></div>
                </div>
                
                <div class="fade-in-item" style="animation-delay: 0.6s">
                  <p class="text-purple-200 font-brand-medium mb-2 text-sm">Date</p>
                  <p class="font-brand-semibold text-xl">28 March 2022</p>
                  <div class="w-full border-t border-white opacity-40 mt-4"></div>
                </div>
                
                <div class="fade-in-item" style="animation-delay: 0.8s">
                  <p class="text-purple-200 font-brand-medium mb-2 text-sm">Address</p>
                  <p class="font-brand-semibold text-xl">75 Main Street, USA</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Project Description -->
          <div class="mb-12 max-w-[60%] scroll-fade-in" ref="descriptionSection">
            <h2 class="text-2xl font-brand-bold text-slate-900 mb-6 slide-in-left">Web Design & Development Solutions</h2>
            
            <div class="prose prose-lg text-slate-600 leading-relaxed space-y-4">
              <p class="fade-in-item" style="animation-delay: 0.2s">
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
              </p>
              
              <p class="fade-in-item" style="animation-delay: 0.4s">
                But I must explain to you how this mistaken idea of denouncing pleasure and praising pain was born and will give you a complete account of the system, and expound the actual teachings of the great explorer of the master-builder of human happiness.
              </p>
              
              <p class="fade-in-item" style="animation-delay: 0.6s">
                Nor again is there anyone who loves or pursues or desires to obtain pain of itself, because it is pain, but because occasionally circumstances occur in which toil and pain can procure him some great pleasure.
                Nor again is there anyone who loves or pursues or desires to obtain pain of itself, because it is pain, but because occasionally circumstances occur in which toil and pain can procure him some great pleasure.
              </p>
            </div>
          </div>

          <!-- Three BIGGER Uniform Images -->
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16 scroll-fade-in" ref="imagesSection">
            <div class="w-full h-80 overflow-hidden rounded-lg shadow-lg slide-in-up" style="animation-delay: 0.1s">
              <img 
                src="https://images.unsplash.com/photo-1551434678-e076c223a692?auto=format&fit=crop&w=600&q=80" 
                alt="Analytics Dashboard View" 
                class="w-full h-full object-cover hover:scale-105 transition-transform duration-300"
              />
            </div>
            <div class="w-full h-80 overflow-hidden rounded-lg shadow-lg slide-in-up" style="animation-delay: 0.3s">
              <img 
                src="https://images.unsplash.com/photo-1504868584819-f8e8b4b6d7e3?auto=format&fit=crop&w=600&q=80" 
                alt="Mobile Interface Design" 
                class="w-full h-full object-cover hover:scale-105 transition-transform duration-300"
              />
            </div>
            <div class="w-full h-80 overflow-hidden rounded-lg shadow-lg slide-in-up" style="animation-delay: 0.5s">
              <img 
                src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=600&q=80" 
                alt="Station Management System" 
                class="w-full h-full object-cover hover:scale-105 transition-transform duration-300"
              />
            </div>
          </div>

          <!-- ENHANCED PROFESSIONAL TECHNOLOGY SECTION -->
          <div class="mb-16 bg-gradient-to-br from-blue-50 via-purple-50 to-indigo-50 rounded-2xl py-20 px-8 border border-gray-100 scroll-fade-in" ref="technologySection">
            <h2 class="text-3xl font-brand-bold text-slate-800 mb-16 text-center slide-in-up">Built Using Trusted Technology From</h2>
            
            <div class="flex flex-wrap justify-center items-center gap-20 lg:gap-24">
              <div class="w-40 h-40 flex items-center justify-center bg-white/80 backdrop-blur-sm rounded-2xl shadow-sm border border-white/50 hover:shadow-lg transition-all duration-300 professional-logo-1">
                <img 
                  src="/l1.png" 
                  alt="Technology Logo 1" 
                  class="max-w-32 max-h-32 object-contain transition-all duration-300"
                />
              </div>
              
              <div class="w-40 h-40 flex items-center justify-center bg-white/80 backdrop-blur-sm rounded-2xl shadow-sm border border-white/50 hover:shadow-lg transition-all duration-300 professional-logo-2">
                <img 
                  src="/l2.png" 
                  alt="Technology Logo 2" 
                  class="max-w-32 max-h-32 object-contain transition-all duration-300"
                />
              </div>
              
              <div class="w-40 h-40 flex items-center justify-center bg-white/80 backdrop-blur-sm rounded-2xl shadow-sm border border-white/50 hover:shadow-lg transition-all duration-300 professional-logo-3">
                <img 
                  src="/l3.png" 
                  alt="Technology Logo 3" 
                  class="max-w-32 max-h-32 object-contain transition-all duration-300"
                />
              </div>
              
              <div class="w-40 h-40 flex items-center justify-center bg-white/80 backdrop-blur-sm rounded-2xl shadow-sm border border-white/50 hover:shadow-lg transition-all duration-300 professional-logo-4">
                <img 
                  src="/l4.png" 
                  alt="Technology Logo 4" 
                  class="max-w-32 max-h-32 object-contain transition-all duration-300"
                />
              </div>
            </div>
          </div>

          <!-- Projects Summary Section -->
          <div class="scroll-fade-in" ref="summarySection">
            <h2 class="text-2xl font-brand-bold text-slate-900 mb-6 slide-in-left">Projects Summary</h2>
            
            <div class="prose prose-lg max-w-none text-slate-600 leading-relaxed">
              <p class="fade-in-item" style="animation-delay: 0.2s">
                At the very heart, we specialize with integrated and skilled work; we are a plug-and-play standard by the makers of excellent of the internet, we build for you and we deliver the best.
              </p>
              
              <p class="mt-4 fade-in-item" style="animation-delay: 0.4s">
                Our commitment to excellence in web design and development ensures that every project we undertake is completed to the highest standards.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const pageLoaded = ref(false)
const visibleSections = ref(new Set())

// Refs for sections
const pageContainer = ref(null)
const headerSection = ref(null)
const mainSection = ref(null)
const heroImageSection = ref(null)
const descriptionSection = ref(null)
const imagesSection = ref(null)
const technologySection = ref(null)
const summarySection = ref(null)

let intersectionObserver = null

useHead({
  title: 'Station Point Pro - Project Details | Station List Pro',
  meta: [
    { 
      name: 'description', 
      content: 'Detailed view of Station Point Pro project featuring advanced web design and development solutions for station management systems.' 
    }
  ]
})

onMounted(() => {
  // Page load animation
  setTimeout(() => {
    pageLoaded.value = true
  }, 100)

  // Intersection Observer for scroll animations
  intersectionObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible')
          // Add section to visible set
          const sectionName = entry.target.getAttribute('ref') || entry.target.id
          if (sectionName) {
            visibleSections.value.add(sectionName)
          }
        }
      })
    },
    {
      threshold: 0.15,
      rootMargin: '0px 0px -50px 0px'
    }
  )

  // Observe all sections
  const sectionsToObserve = [
    heroImageSection.value,
    descriptionSection.value,
    imagesSection.value,
    technologySection.value,
    summarySection.value
  ]

  sectionsToObserve.forEach(section => {
    if (section) {
      intersectionObserver.observe(section)
    }
  })

  console.log('Station Point Pro project page loaded successfully')
})

onUnmounted(() => {
  if (intersectionObserver) {
    intersectionObserver.disconnect()
  }
})
</script>

<style scoped>
/* PAGE LOAD ANIMATIONS */
.page-container {
  opacity: 0;
  transform: translateY(20px);
  transition: all 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.page-container.page-loaded {
  opacity: 1;
  transform: translateY(0);
}

/* SCROLL ANIMATIONS */
.scroll-fade-in {
  opacity: 0;
  transform: translateY(40px);
  transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.scroll-fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}

.slide-in-left {
  opacity: 0;
  transform: translateX(-50px);
  animation: slideInLeft 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
  animation-delay: 0.3s;
}

.slide-in-right {
  opacity: 0;
  transform: translateX(50px);
  animation: slideInRight 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
  animation-delay: 0.5s;
}

.slide-in-up {
  opacity: 0;
  transform: translateY(50px);
  animation: slideInUp 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
}

.fade-in-item {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInItem 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
}

/* SCROLL-TRIGGERED ANIMATIONS */
.scroll-fade-in.visible .slide-in-up,
.scroll-fade-in.visible .fade-in-item {
  animation-play-state: running;
}

/* KEYFRAMES */
@keyframes slideInLeft {
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInItem {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ENHANCED floating animations - MORE MOVEMENT for header circles */
@keyframes float-enhanced {
  0%, 100% { 
    transform: translateY(0px) rotate(0deg);
    opacity: 0.7;
  }
  50% { 
    transform: translateY(-20px) rotate(10deg);
    opacity: 1;
  }
}

@keyframes float-enhanced-delayed {
  0%, 100% { 
    transform: translateY(0px) rotate(0deg);
    opacity: 0.6;
  }
  50% { 
    transform: translateY(-18px) rotate(-10deg);
    opacity: 1;
  }
}

@keyframes float-enhanced-slow {
  0%, 100% { 
    transform: translateY(0px) scale(1);
    opacity: 0.5;
  }
  50% { 
    transform: translateY(-15px) scale(1.1);
    opacity: 0.9;
  }
}

@keyframes float-enhanced-bounce {
  0%, 100% { 
    transform: translateY(0px) scale(1) rotate(0deg);
    opacity: 0.6;
  }
  25% { 
    transform: translateY(-10px) scale(1.05) rotate(2deg);
    opacity: 0.8;
  }
  50% { 
    transform: translateY(-22px) scale(1.1) rotate(-2deg);
    opacity: 1;
  }
  75% { 
    transform: translateY(-8px) scale(1.05) rotate(1deg);
    opacity: 0.8;
  }
}

/* ENHANCED PROFESSIONAL LOGO ANIMATIONS - MORE NOTICEABLE */
@keyframes professional-float-1 {
  0%, 100% {
    transform: translateY(0px) scale(1);
  }
  50% {
    transform: translateY(-12px) scale(1.02);
  }
}

@keyframes professional-float-2 {
  0%, 100% {
    transform: translateY(0px) scale(1);
  }
  50% {
    transform: translateY(-15px) scale(1.03);
  }
}

@keyframes professional-float-3 {
  0%, 100% {
    transform: translateY(0px) scale(1);
  }
  50% {
    transform: translateY(-10px) scale(1.02);
  }
}

@keyframes professional-float-4 {
  0%, 100% {
    transform: translateY(0px) scale(1);
  }
  50% {
    transform: translateY(-14px) scale(1.04);
  }
}

.animate-float-enhanced {
  animation: float-enhanced 4s ease-in-out infinite;
}

.animate-float-enhanced-delayed {
  animation: float-enhanced-delayed 5s ease-in-out infinite;
  animation-delay: 1.5s;
}

.animate-float-enhanced-slow {
  animation: float-enhanced-slow 6s ease-in-out infinite;
  animation-delay: 0.8s;
}

.animate-float-enhanced-bounce {
  animation: float-enhanced-bounce 7s ease-in-out infinite;
  animation-delay: 2s;
}

/* Individual Professional Logo Animations - FIXED VISIBILITY */
.professional-logo-1,
.professional-logo-2,
.professional-logo-3,
.professional-logo-4 {
  opacity: 1; /* Ensure they're visible */
}

.professional-logo-1 {
  animation: professional-float-1 4.2s ease-in-out infinite;
}

.professional-logo-2 {
  animation: professional-float-2 3.8s ease-in-out infinite;
  animation-delay: 0.7s;
}

.professional-logo-3 {
  animation: professional-float-3 4.5s ease-in-out infinite;
  animation-delay: 1.2s;
}

.professional-logo-4 {
  animation: professional-float-4 3.5s ease-in-out infinite;
  animation-delay: 1.8s;
}

/* Enhanced Hover Effects */
.professional-logo-1:hover {
  transform: translateY(-18px) scale(1.06);
}

.professional-logo-2:hover {
  transform: translateY(-20px) scale(1.07);
}

.professional-logo-3:hover {
  transform: translateY(-16px) scale(1.05);
}

.professional-logo-4:hover {
  transform: translateY(-22px) scale(1.08);
}

/* SMOOTH SCROLLING */
html {
  scroll-behavior: smooth;
}

/* Other styles */
.prose p:last-child {
  margin-bottom: 0;
}

img {
  transition: transform 0.3s ease-in-out;
}

.border-t-4 {
  border-top-width: 4px !important;
}

/* RESPONSIVE DESIGN */
@media (max-width: 1024px) {
  .max-w-\[60\%\] {
    max-width: 100%;
  }
}

@media (max-width: 768px) {
  .prose {
    font-size: 1rem;
    line-height: 1.6;
  }
  
  .professional-logo-1, 
  .professional-logo-2, 
  .professional-logo-3, 
  .professional-logo-4 {
    animation: none;
  }
  
  .slide-in-left,
  .slide-in-right,
  .slide-in-up,
  .fade-in-item {
    animation: none;
    opacity: 1;
    transform: none;
  }
}

.shadow-xl {
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* PERFORMANCE OPTIMIZATION */
.animate-float-enhanced,
.animate-float-enhanced-delayed,
.animate-float-enhanced-slow,
.animate-float-enhanced-bounce,
.professional-logo-1,
.professional-logo-2,
.professional-logo-3,
.professional-logo-4 {
  will-change: transform;
}

/* ACCESSIBILITY */
@media (prefers-reduced-motion: reduce) {
  .page-container,
  .scroll-fade-in,
  .slide-in-left,
  .slide-in-right,
  .slide-in-up,
  .fade-in-item,
  .animate-float-enhanced,
  .animate-float-enhanced-delayed,
  .animate-float-enhanced-slow,
  .animate-float-enhanced-bounce,
  .professional-logo-1,
  .professional-logo-2,
  .professional-logo-3,
  .professional-logo-4 {
    animation: none;
    transition: none;
    opacity: 1;
    transform: none;
  }
}
</style>
