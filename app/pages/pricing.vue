<!-- app/pages/pricing.vue -->
<template>
  <div class="min-h-screen bg-gradient-to-br from-primary via-accentlight to-primary py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <!-- Header Section -->
      <div 
        class="text-center mb-16 opacity-0 translate-y-8 animate-fade-in-up"
        :style="{ animationDelay: '0.1s' }"
      >
        <h1 class="text-5xl md:text-6xl font-brand font-brand-bold text-text-primary mb-6 leading-tight">
          Choose Your 
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-accent to-purple-600">
            Perfect Plan
          </span>
        </h1>
        <p class="text-xl text-text-secondary max-w-3xl mx-auto font-brand leading-relaxed">
          Scale your business with our flexible pricing options. Start free and upgrade as you grow.
        </p>
        
        <!-- Billing Toggle -->
        <div 
          class="flex items-center justify-center mt-10 space-x-4 opacity-0 translate-y-4 animate-fade-in-up"
          :style="{ animationDelay: '0.3s' }"
        >
          <span class="text-text-secondary font-brand font-brand-medium transition-all duration-300" 
                :class="{ 'text-text-primary font-brand-semibold': !isYearly }">
            Monthly
          </span>
          <button 
            @click="toggleBilling"
            class="relative inline-flex h-8 w-16 items-center rounded-full transition-colors duration-300 ease-in-out focus:outline-none focus:ring-4 focus:ring-accent/20 hover:scale-105 transform"
            :class="isYearly ? 'bg-accent' : 'bg-gray-300'"
          >
            <span class="sr-only">Toggle billing period</span>
            <span 
              class="inline-block h-6 w-6 transform rounded-full bg-white shadow-lg transition-transform duration-300 ease-in-out"
              :class="isYearly ? 'translate-x-9' : 'translate-x-1'"
            ></span>
          </button>
          <span class="text-text-secondary font-brand font-brand-medium flex items-center space-x-2 transition-all duration-300"
                :class="{ 'text-text-primary font-brand-semibold': isYearly }">
            <span>Yearly</span>
            <span class="bg-gradient-to-r from-accent to-accent text-primary px-2 py-1 rounded-full text-xs font-brand-semibold animate-pulse">
              Save 20%
            </span>
          </span>
        </div>
      </div>

      <!-- Pricing Cards - Equal Height with Consistent Features -->
      <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-8 lg:gap-6 items-stretch" ref="pricingCards">
        
        <!-- Free Plan -->
        <div 
          class="relative bg-primary rounded-3xl shadow-xl border border-border p-8 transition-all duration-700 ease-out hover:shadow-2xl hover:-translate-y-2 opacity-0 translate-y-8 animate-fade-in-up flex flex-col scroll-animate"
          :style="{ animationDelay: '0.4s' }"
        >
          <div class="text-center flex-grow flex flex-col">
            <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Free</h3>
            <p class="text-text-secondary mb-6 font-brand">Get started with basic features</p>
            
            <div class="mb-8 transform transition-all duration-300 hover:scale-105">
              <span class="text-5xl font-brand font-brand-bold text-text-primary">
                $0
              </span>
              <span class="text-text-secondary font-brand">/month</span>
              <div class="text-sm text-accent font-brand-medium mt-1">
                Forever free
              </div>
            </div>

            <ul class="space-y-4 mb-8 text-left flex-grow">
              <li 
                v-for="(feature, index) in uniformFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.6 + index * 0.1}s` }"
              >
                <div v-if="feature.values[0] === 'x'" class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <div v-else class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-accent" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <span class="text-text-secondary font-brand">{{ feature.name }}: {{ feature.values[0] === 'x' ? 'Not available' : feature.values[0] }}</span>
              </li>
            </ul>

            <button class="w-full bg-gray-200 hover:bg-gray-300 text-text-primary font-brand font-brand-semibold py-4 px-6 rounded-xl transition-all duration-300 hover:scale-105 transform hover:shadow-lg mt-auto">
              Get Started Free
            </button>
          </div>
        </div>

        <!-- Starter Plan -->
        <div 
          class="relative bg-primary rounded-3xl shadow-xl border border-border p-8 transition-all duration-700 ease-out hover:shadow-2xl hover:-translate-y-2 opacity-0 translate-y-8 animate-fade-in-up flex flex-col scroll-animate"
          :style="{ animationDelay: '0.5s' }"
        >
          <div class="text-center flex-grow flex flex-col">
            <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Starter</h3>
            <p class="text-text-secondary mb-6 font-brand">Perfect for individuals and small projects</p>
            
            <div class="mb-8 transform transition-all duration-300 hover:scale-105">
              <span class="text-5xl font-brand font-brand-bold text-text-primary">
                ${{ isYearly ? '8' : '10' }}
              </span>
              <span class="text-text-secondary font-brand">/month</span>
              <div v-if="isYearly" class="text-sm text-accent font-brand-medium mt-1 animate-slide-in-left">
                Billed annually ($96/year)
              </div>
            </div>

            <ul class="space-y-4 mb-8 text-left flex-grow">
              <li 
                v-for="(feature, index) in uniformFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.7 + index * 0.1}s` }"
              >
                <div v-if="feature.values[1] === 'x'" class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <div v-else class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-accent" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <span class="text-text-secondary font-brand">{{ feature.name }}: {{ feature.values[1] === 'x' ? 'Not available' : feature.values[1] }}</span>
              </li>
            </ul>

            <button class="w-full bg-accentlight hover:bg-accent hover:text-primary text-text-primary font-brand font-brand-semibold py-4 px-6 rounded-xl transition-all duration-300 hover:scale-105 transform hover:shadow-lg mt-auto">
              Get Started
            </button>
          </div>
        </div>

        <!-- Professional Plan (Popular) -->
        <div 
          class="relative bg-primary rounded-3xl shadow-2xl border-2 border-accent p-8 pt-12 pb-8 transition-all duration-700 ease-out hover:shadow-3xl hover:-translate-y-3 opacity-0 translate-y-8 animate-fade-in-up flex flex-col scroll-animate"
          :style="{ animationDelay: '0.6s' }"
        >
          <!-- Popular Badge -->
          <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 animate-bounce-slow">
            <span class="bg-gradient-to-r from-accent to-accent text-primary px-6 py-2 rounded-full text-sm font-brand font-brand-bold shadow-lg animate-glow">
              Most Popular
            </span>
          </div>
          
          <div class="text-center flex-grow flex flex-col">
            <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Professional</h3>
            <p class="text-text-secondary mb-6 font-brand">Ideal for growing businesses and teams</p>
            
            <div class="mb-8 transform transition-all duration-300 hover:scale-105">
              <span class="text-5xl font-brand font-brand-bold text-accent animate-number-counter">
                ${{ isYearly ? '24' : '30' }}
              </span>
              <span class="text-text-secondary font-brand">/month</span>
              <div v-if="isYearly" class="text-sm text-accent font-brand-medium mt-1 animate-slide-in-left">
                Billed annually ($288/year)
              </div>
            </div>

            <ul class="space-y-4 mb-8 text-left flex-grow">
              <li 
                v-for="(feature, index) in uniformFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.8 + index * 0.1}s` }"
              >
                <div v-if="feature.values[2] === 'x'" class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <div v-else class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-accent" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <span class="text-text-secondary font-brand">{{ feature.name }}: {{ feature.values[2] === 'x' ? 'Not available' : feature.values[2] }}</span>
              </li>
            </ul>

            <button class="w-full bg-gradient-to-r from-accent to-accent hover:opacity-90 text-primary font-brand font-brand-bold py-4 px-6 rounded-xl transition-all duration-300 hover:scale-105 shadow-lg hover:shadow-xl transform animate-gradient-shift mt-auto">
              Start Free Trial
            </button>
          </div>
        </div>

        <!-- Enterprise Plan -->
        <div 
          class="relative bg-primary rounded-3xl shadow-xl border border-border p-8 transition-all duration-700 ease-out hover:shadow-2xl hover:-translate-y-2 opacity-0 translate-y-8 animate-fade-in-up flex flex-col scroll-animate"
          :style="{ animationDelay: '0.7s' }"
        >
          <div class="text-center flex-grow flex flex-col">
            <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Enterprise</h3>
            <p class="text-text-secondary mb-6 font-brand">Advanced features for large organizations</p>
            
            <div class="mb-8 transform transition-all duration-300 hover:scale-105">
              <span class="text-5xl font-brand font-brand-bold text-text-primary">
                ${{ isYearly ? '80' : '100' }}
              </span>
              <span class="text-text-secondary font-brand">/month</span>
              <div v-if="isYearly" class="text-sm text-accent font-brand-medium mt-1 animate-slide-in-left">
                Billed annually ($960/year)
              </div>
            </div>

            <ul class="space-y-4 mb-8 text-left flex-grow">
              <li 
                v-for="(feature, index) in uniformFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.9 + index * 0.1}s` }"
              >
                <div v-if="feature.values[3] === 'x'" class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <div v-else class="w-5 h-5 flex items-center justify-center mr-3 flex-shrink-0">
                  <svg class="w-5 h-5 text-accent" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                  </svg>
                </div>
                <span class="text-text-secondary font-brand">{{ feature.name }}: {{ feature.values[3] === 'x' ? 'Not available' : feature.values[3] }}</span>
              </li>
            </ul>

            <button class="w-full bg-dark hover:bg-darker text-primary font-brand font-brand-semibold py-4 px-6 rounded-xl transition-all duration-300 hover:scale-105 transform hover:shadow-lg mt-auto">
              Contact Sales
            </button>
          </div>
        </div>
      </div>

      <!-- Enhanced Feature Comparison Section -->
      <div 
        class="mt-24 opacity-0 translate-y-8 animate-fade-in-up scroll-animate"
        :style="{ animationDelay: '1.0s' }"
        ref="comparisonSection"
      >
        <div class="text-center mb-12">
          <h2 class="text-4xl font-brand font-brand-bold text-text-primary mb-4">
            Compare All Features
          </h2>
          <p class="text-xl text-text-secondary font-brand max-w-3xl mx-auto">
            See exactly what's included in each plan to make the best choice for your needs.
          </p>
        </div>

        <div class="bg-primary rounded-3xl shadow-xl border border-border overflow-hidden">
          <div class="overflow-x-auto">
            <table class="w-full">
              <thead>
                <tr class="bg-accentlight">
                  <th class="text-left py-6 px-6 font-brand font-brand-semibold text-text-primary text-lg">
                    Features
                    <div class="text-sm text-text-secondary font-brand-medium font-normal mt-1">What's included</div>
                  </th>
                  <th class="text-center py-6 px-4 font-brand font-brand-semibold text-text-primary">
                    <div class="text-lg">Free</div>
                    <div class="text-2xl font-brand-bold mt-1">$0</div>
                    <div class="text-xs text-text-secondary">per month</div>
                  </th>
                  <th class="text-center py-6 px-4 font-brand font-brand-semibold text-text-primary">
                    <div class="text-lg">Starter</div>
                    <div class="text-2xl font-brand-bold mt-1">${{ isYearly ? '8' : '10' }}</div>
                    <div class="text-xs text-text-secondary">per month</div>
                  </th>
                  <th class="text-center py-6 px-4 font-brand font-brand-semibold text-accent bg-accent/5 relative">
                    <div class="absolute -top-2 left-1/2 transform -translate-x-1/2">
                      <span class="bg-accent text-primary px-3 py-1 rounded-full text-xs font-brand-bold">POPULAR</span>
                    </div>
                    <div class="text-lg text-accent">Professional</div>
                    <div class="text-2xl font-brand-bold mt-1 text-accent">${{ isYearly ? '24' : '30' }}</div>
                    <div class="text-xs text-accent/80">per month</div>
                  </th>
                  <th class="text-center py-6 px-4 font-brand font-brand-semibold text-text-primary">
                    <div class="text-lg">Enterprise</div>
                    <div class="text-2xl font-brand-bold mt-1">${{ isYearly ? '80' : '100' }}</div>
                    <div class="text-xs text-text-secondary">per month</div>
                  </th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="(feature, index) in comparisonFeatures" :key="index" class="border-t border-border hover:bg-accentlight/20 transition-colors">
                  <td class="py-5 px-6 font-brand text-text-primary">
                    <div class="font-brand-semibold text-base">{{ feature.name }}</div>
                    <div class="text-sm text-text-secondary mt-1">{{ feature.description }}</div>
                  </td>
                  
                  <!-- Free Column -->
                  <td class="py-5 px-4 text-center">
                    <div v-if="feature.free === false" class="w-6 h-6 bg-gray-100 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else-if="feature.free === true" class="w-6 h-6 bg-accent/20 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-accent" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else>
                      <span class="inline-block bg-gray-100 text-gray-600 px-3 py-1 rounded-lg text-sm font-brand-medium">{{ feature.free }}</span>
                    </div>
                  </td>
                  
                  <!-- Starter Column -->
                  <td class="py-5 px-4 text-center">
                    <div v-if="feature.starter === false" class="w-6 h-6 bg-gray-100 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else-if="feature.starter === true" class="w-6 h-6 bg-accent/20 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-accent" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else>
                      <span class="inline-block bg-blue-100 text-blue-600 px-3 py-1 rounded-lg text-sm font-brand-medium">{{ feature.starter }}</span>
                    </div>
                  </td>
                  
                  <!-- Professional Column (Highlighted) -->
                  <td class="py-5 px-4 text-center bg-accent/5">
                    <div v-if="feature.professional === false" class="w-6 h-6 bg-gray-100 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else-if="feature.professional === true" class="w-6 h-6 bg-accent/20 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-accent" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else>
                      <span class="inline-block bg-accent/20 text-accent px-3 py-1 rounded-lg text-sm font-brand-medium">{{ feature.professional }}</span>
                    </div>
                  </td>
                  
                  <!-- Enterprise Column -->
                  <td class="py-5 px-4 text-center">
                    <div v-if="feature.enterprise === false" class="w-6 h-6 bg-gray-100 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else-if="feature.enterprise === true" class="w-6 h-6 bg-accent/20 rounded-full flex items-center justify-center mx-auto">
                      <svg class="w-4 h-4 text-accent" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                      </svg>
                    </div>
                    <div v-else>
                      <span class="inline-block bg-gray-100 text-gray-600 px-3 py-1 rounded-lg text-sm font-brand-medium">{{ feature.enterprise }}</span>
                    </div>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>

      <!-- Testimonials Section -->
      <div 
        class="mt-24 opacity-0 translate-y-8 animate-fade-in-up scroll-animate"
        :style="{ animationDelay: '1.1s' }"
        ref="testimonialsSection"
      >
        <div class="text-center mb-12">
          <h2 class="text-4xl font-brand font-brand-bold text-text-primary mb-4">
            What Our Customers Say
          </h2>
          <p class="text-xl text-text-secondary font-brand max-w-3xl mx-auto">
            Join thousands of satisfied customers who trust our platform.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div 
            v-for="(testimonial, index) in testimonials" 
            :key="index"
            class="bg-primary rounded-2xl shadow-lg border border-border p-8 opacity-0 translate-y-4 animate-fade-in-up hover-lift scroll-animate"
            :style="{ animationDelay: `${1.3 + index * 0.1}s` }"
          >
            <div class="mb-6">
              <div class="flex text-accent mb-4">
                <svg v-for="i in 5" :key="i" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
                </svg>
              </div>
              <p class="text-text-secondary font-brand leading-relaxed italic">
                "{{ testimonial.quote }}"
              </p>
            </div>
            <div class="flex items-center">
              <img :src="testimonial.avatar" :alt="testimonial.name" class="w-12 h-12 rounded-full mr-4">
              <div>
                <p class="font-brand font-brand-semibold text-text-primary">{{ testimonial.name }}</p>
                <p class="text-text-secondary font-brand text-sm">{{ testimonial.role }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- FAQ Section -->
      <div 
        class="mt-24 text-center opacity-0 translate-y-8 animate-fade-in-up scroll-animate mb-16"
        :style="{ animationDelay: '1.2s' }"
        ref="faqSection"
      >
        <h2 class="text-3xl font-brand font-brand-bold text-text-primary mb-4">
          Frequently Asked Questions
        </h2>
        <p class="text-text-secondary font-brand mb-12 max-w-2xl mx-auto">
          Everything you need to know about our pricing and plans
        </p>
        
        <div class="max-w-5xl mx-auto space-y-4">
          <div 
            v-for="(faq, index) in faqs" 
            :key="index"
            class="bg-primary rounded-2xl shadow-lg border border-border overflow-hidden opacity-0 translate-y-4 animate-fade-in-up transform transition-all duration-500 ease-out hover:scale-[1.02] scroll-animate"
            :style="{ animationDelay: `${1.4 + index * 0.1}s` }"
          >
            <button 
              @click="toggleFAQ(index)" 
              class="w-full p-6 text-left flex items-center justify-between hover:bg-accentlight transition-colors duration-300 ease-out"
            >
              <div class="flex items-center space-x-4">
                <div class="flex-shrink-0">
                  <svg 
                    class="w-5 h-5 text-accent transition-transform duration-500 ease-out" 
                    :class="{ 'rotate-45': openFAQ === index }"
                    fill="none" 
                    stroke="currentColor" 
                    viewBox="0 0 24 24"
                  >
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path>
                  </svg>
                </div>
                <h3 class="font-brand font-brand-semibold text-text-primary text-lg">{{ faq.question }}</h3>
              </div>
            </button>
            <Transition
              name="expand"
              enter-active-class="transition-all duration-500 ease-out"
              leave-active-class="transition-all duration-300 ease-in"
              enter-from-class="opacity-0 max-h-0 transform -translate-y-2"
              enter-to-class="opacity-100 max-h-40 transform translate-y-0"
              leave-from-class="opacity-100 max-h-40 transform translate-y-0"
              leave-to-class="opacity-0 max-h-0 transform -translate-y-2"
            >
              <div 
                v-show="openFAQ === index" 
                class="px-6 pb-6 border-t border-border bg-accentlight"
              >
                <div class="pl-9 pt-4">
                  <p class="text-text-secondary font-brand leading-relaxed">
                    {{ faq.answer }}
                  </p>
                </div>
              </div>
            </Transition>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isYearly = ref(false)
const openFAQ = ref(null)

// Refs for scroll animations
const pricingCards = ref(null)
const comparisonSection = ref(null)
const testimonialsSection = ref(null)
const faqSection = ref(null)

let scrollObserver = null

// Uniform features for all plans with consistent structure
const uniformFeatures = [
  { name: 'Projects', values: ['2', '5', 'Unlimited', 'Unlimited'] },
  { name: 'Storage', values: ['1GB', '10GB', '100GB', 'Unlimited'] },
  { name: 'Team Members', values: ['x', '3', '10', 'Unlimited'] },
  { name: 'Analytics', values: ['x', '✓', '✓', '✓'] },
  { name: 'Priority Support', values: ['x', 'x', '✓', '✓'] },
  { name: 'Custom Integrations', values: ['x', 'x', '✓', '✓'] },
  { name: 'API Access', values: ['x', 'x', '✓', '✓'] },
  { name: 'White Label', values: ['x', 'x', 'x', '✓'] }
]

// Enhanced comparison features with descriptions (for table)
const comparisonFeatures = [
  { name: 'Projects', description: 'Number of active projects you can manage', free: '2', starter: '5', professional: 'Unlimited', enterprise: 'Unlimited' },
  { name: 'Storage', description: 'Available file storage space', free: '1GB', starter: '10GB', professional: '100GB', enterprise: 'Unlimited' },
  { name: 'Team Members', description: 'Maximum team size for collaboration', free: false, starter: '3', professional: '10', enterprise: 'Unlimited' },
  { name: 'Analytics', description: 'Performance insights and reporting tools', free: false, starter: true, professional: true, enterprise: true },
  { name: 'Priority Support', description: '24/7 priority customer assistance', free: false, starter: false, professional: true, enterprise: true },
  { name: 'Custom Integrations', description: 'Third-party app integrations', free: false, starter: false, professional: true, enterprise: true },
  { name: 'API Access', description: 'Developer API for custom solutions', free: false, starter: false, professional: true, enterprise: true },
  { name: 'White Label', description: 'Brand customization options', free: false, starter: false, professional: false, enterprise: true },
]

const testimonials = [
  {
    quote: "This platform has completely transformed how we manage our projects. The professional plan gives us everything we need.",
    name: "Sarah Johnson",
    role: "CEO, TechStart",
    avatar: "https://images.unsplash.com/photo-1494790108755-2616b612b55c?w=150&h=150&fit=crop&crop=face"
  },
  {
    quote: "Amazing value for money. We started with the starter plan and quickly upgraded as our team grew.",
    name: "Michael Chen",
    role: "Product Manager, InnovateCorp",
    avatar: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=150&h=150&fit=crop&crop=face"
  },
  {
    quote: "The enterprise features and support are outstanding. Our dedicated account manager is incredibly helpful.",
    name: "Emily Rodriguez",
    role: "CTO, GlobalTech",
    avatar: "https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=150&h=150&fit=crop&crop=face"
  }
]

const faqs = [
  {
    question: 'Can I change my plan anytime?',
    answer: 'Yes, you can upgrade or downgrade your plan at any time. Changes take effect immediately and you\'ll be charged or credited the prorated amount. There are no long-term contracts or cancellation fees.'
  },
  {
    question: 'Is there a free trial?',
    answer: 'We offer a 14-day free trial for the Professional plan with full access to all features. No credit card required to start. You can cancel anytime during the trial period without being charged.'
  },
  {
    question: 'What payment methods do you accept?',
    answer: 'We accept all major credit cards (Visa, MasterCard, American Express), PayPal, and bank transfers for Enterprise plans. All payments are processed securely and encrypted.'
  },
  {
    question: 'Do you offer refunds?',
    answer: 'Yes, we offer a 30-day money-back guarantee for all paid plans. If you\'re not completely satisfied, contact our support team for a full refund within the first 30 days of your subscription.'
  },
  {
    question: 'Can I get a custom plan for my organization?',
    answer: 'Absolutely! For large organizations with specific needs, we can create custom plans with tailored features, pricing, and support options. Contact our sales team to discuss your requirements.'
  }
]

const toggleBilling = () => {
  isYearly.value = !isYearly.value
}

const toggleFAQ = (index) => {
  openFAQ.value = openFAQ.value === index ? null : index
}

// Enhanced scroll animations
const setupScrollAnimations = () => {
  scrollObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in')
          entry.target.style.opacity = '1'
          entry.target.style.transform = 'translateY(0)'
        }
      })
    },
    {
      threshold: 0.1,
      rootMargin: '0px 0px -100px 0px'
    }
  )

  // Observe all scroll-animate elements
  const scrollElements = document.querySelectorAll('.scroll-animate')
  scrollElements.forEach(el => {
    if (scrollObserver) {
      scrollObserver.observe(el)
    }
  })
}

onMounted(() => {
  // Trigger initial animations
  const animatedElements = document.querySelectorAll('[class*="animate-"]')
  animatedElements.forEach(el => {
    el.style.animationFillMode = 'forwards'
  })

  // Setup scroll animations after a delay
  setTimeout(() => {
    setupScrollAnimations()
  }, 1000)
})

onUnmounted(() => {
  if (scrollObserver) {
    scrollObserver.disconnect()
  }
})
</script>

<style scoped>
@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(2rem); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes slide-in-right {
  from { opacity: 0; transform: translateX(1rem); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes slide-in-left {
  from { opacity: 0; transform: translateX(-1rem); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes bounce-slow {
  0%, 100% { transform: translateY(0) translateX(-50%); }
  50% { transform: translateY(-5px) translateX(-50%); }
}

@keyframes glow {
  0%, 100% { box-shadow: 0 0 5px rgba(var(--accent), 0.5); }
  50% { box-shadow: 0 0 20px rgba(var(--accent), 0.8); }
}

@keyframes number-counter {
  from { opacity: 0; transform: scale(0.8); }
  to { opacity: 1; transform: scale(1); }
}

@keyframes gradient-shift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.animate-fade-in-up { animation: fade-in-up 0.8s ease-out both; }
.animate-slide-in-right { animation: slide-in-right 0.7s ease-out both; }
.animate-slide-in-left { animation: slide-in-left 0.7s ease-out both; }
.animate-bounce-slow { animation: bounce-slow 3s ease-in-out infinite; }
.animate-glow { animation: glow 2s ease-in-out infinite; }
.animate-number-counter { animation: number-counter 1s ease-out both; }
.animate-gradient-shift { background-size: 200% 200%; animation: gradient-shift 3s ease infinite; }

/* Enhanced scroll animations */
.scroll-animate {
  transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.scroll-animate.animate-in {
  opacity: 1 !important;
  transform: translateY(0) !important;
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Enhanced hover effects */
.hover-lift {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

/* Performance optimizations */
.animate-fade-in-up,
.animate-slide-in-right,
.animate-slide-in-left,
.animate-bounce-slow,
.animate-glow,
.animate-number-counter,
.animate-gradient-shift {
  will-change: transform, opacity;
}

@media (max-width: 1280px) {
  .xl\:grid-cols-4 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
}

@media (max-width: 768px) {
  .md\:grid-cols-2 { grid-template-columns: repeat(1, minmax(0, 1fr)); }
}

/* Reduced motion accessibility */
@media (prefers-reduced-motion: reduce) {
  .animate-fade-in-up,
  .animate-slide-in-right,
  .animate-slide-in-left,
  .animate-bounce-slow,
  .animate-glow,
  .animate-number-counter,
  .animate-gradient-shift,
  .scroll-animate {
    animation: none;
    transition: none;
    opacity: 1;
    transform: none;
  }
}
</style>
