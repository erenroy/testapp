<template>
  <div class="page-container">
    <!-- Hero Section -->
    <main class="max-w-none mx-auto px-16 flex flex-col md:flex-row items-center gap-12 md:gap-16 py-24">
      <!-- Left content -->
      <div class="flex-1 w-full max-w-2xl">
        <!-- Decorative dots -->
        <div class="flex gap-1 mb-6">
          <div class="w-2 h-2 bg-accentlight rounded-full"></div>
          <div class="w-2 h-2 bg-accentlight rounded-full"></div>
          <div class="w-2 h-2 bg-accentlight rounded-full"></div>
        </div>
        
        <span class="inline-block px-5 py-2 rounded-lg bg-accentlight text-accent font-brand-medium text-sm mb-6">Saaslanding Agency</span>
        
        <h1 class="text-5xl md:text-6xl lg:text-7xl font-brand-bold text-darker mb-6 leading-tight">Advanced analytics<br />software solutions</h1>
        
        <p class="text-xl text-text-secondary mb-8 leading-relaxed">Sit amet consectetur adipiscing elit seddo eiusmod tempode dunt ut labore et dolore magna aliqua suspendisse</p>
        
        <ul class="mb-10 space-y-3">
          <li class="flex items-center gap-3 text-lg text-darker">
            <span class="text-accent text-xl">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
                <circle cx="10" cy="10" r="10" fill="#7f56d9"/>
                <path d="M7 10.5l2 2 3.5-3.5" stroke="#fff" stroke-width="2" fill="none"/>
              </svg>
            </span>
            30-day free trial of our premium plan
          </li>
          <li class="flex items-center gap-3 text-lg text-darker">
            <span class="text-accent text-xl">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
                <circle cx="10" cy="10" r="10" fill="#7f56d9"/>
                <path d="M7 10.5l2 2 3.5-3.5" stroke="#fff" stroke-width="2" fill="none"/>
              </svg>
            </span>
            100% Free - No payments required
          </li>
        </ul>
        
        <div class="flex flex-col sm:flex-row gap-5">
          <a href="#" class="px-10 py-4 rounded-lg bg-accent hover:bg-[#6842c2] text-white text-lg font-brand-semibold shadow-lg hover:shadow-xl transition-all duration-300 text-center transform hover:scale-105">Get Started <span class="inline-block ml-2">&rarr;</span></a>
          <a href="#" class="px-10 py-4 rounded-lg bg-accentlight hover:bg-[#ebe7fa] text-accent text-lg font-brand-semibold transition-all duration-300 text-center">Learn More <span class="inline-block ml-2">&rarr;</span></a>
        </div>

        <!-- Decorative star -->
        <div class="mt-8 text-accent">
          <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20">
            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
          </svg>
        </div>
      </div>
      
      <!-- Right image -->
      <div class="flex-1 w-full flex justify-center">
        <img 
          src="https://images.unsplash.com/photo-1513258496099-48168024aec0?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
          alt="Advanced analytics software"
          class="rounded-xl object-cover w-[380px] h-[400px] md:w-[500px] md:h-[520px] lg:w-[600px] lg:h-[620px] xl:w-[700px] xl:h-[720px] border border-border shadow-2xl"
          loading="eager"
        />
      </div>
    </main>

    <!-- Homepage sections -->
    <Headernext />
    <Solutions />
    <UserExperienceSection />
    <Corefeatures />
    <Services />
    <Updates />
    <Feedback />
  </div>
</template>

<script setup>
import UserExperienceSection from '../../components/UserExperienceSection.vue'
import Solutions from '../../components/Solutions.vue'
import Corefeatures from '../../components/Corefeatures.vue'
import Services from '../../components/Services.vue'
import Updates from '../../components/Updates.vue'
import Feedback from '../../components/Feedback.vue'
import Headernext from '../../components/Headernext.vue'
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
</style>
