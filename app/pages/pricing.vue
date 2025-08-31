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

      <!-- Pricing Cards -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 lg:gap-12 items-center">
        
        <!-- Starter Plan -->
        <div 
          class="relative bg-primary rounded-3xl shadow-xl border border-border p-8 transition-all duration-700 ease-out hover:shadow-2xl hover:-translate-y-2 opacity-0 translate-y-8 animate-fade-in-up"
          :style="{ animationDelay: '0.5s' }"
        >
          <div class="text-center">
            <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Starter</h3>
            <p class="text-text-secondary mb-6 font-brand">Perfect for individuals and small projects</p>
            
            <div class="mb-8 transform transition-all duration-300 hover:scale-105">
              <span class="text-5xl font-brand font-brand-bold text-text-primary">
                ${{ isYearly ? '8' : '10' }}
              </span>
              <span class="text-text-secondary font-brand">{{ isYearly ? '/month' : '/month' }}</span>
              <div v-if="isYearly" class="text-sm text-accent font-brand-medium mt-1 animate-slide-in-left">
                Billed annually ($96/year)
              </div>
            </div>

            <ul class="space-y-4 mb-8 text-left">
              <li 
                v-for="(feature, index) in starterFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.7 + index * 0.1}s` }"
              >
                <svg class="w-5 h-5 text-accent mr-3 flex-shrink-0 transform transition-transform duration-300 hover:scale-110" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                </svg>
                <span class="text-text-secondary font-brand">{{ feature }}</span>
              </li>
            </ul>

            <button class="w-full bg-accentlight hover:bg-accent hover:text-primary text-text-primary font-brand font-brand-semibold py-4 px-6 rounded-xl transition-all duration-300 hover:scale-105 transform hover:shadow-lg">
              Get Started
            </button>
          </div>
        </div>

        <!-- Professional Plan (Popular) - Made Taller -->
        <div 
          class="relative bg-primary rounded-3xl shadow-2xl border-2 border-accent p-8 pt-12 pb-12 transform scale-105 transition-all duration-700 ease-out hover:shadow-3xl hover:-translate-y-3 opacity-0 translate-y-8 animate-fade-in-up min-h-[600px] flex flex-col justify-between"
          :style="{ animationDelay: '0.6s' }"
        >
          <!-- Popular Badge -->
          <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 animate-bounce-slow">
            <span class="bg-gradient-to-r from-accent to-accent text-primary px-6 py-2 rounded-full text-sm font-brand font-brand-bold shadow-lg animate-glow">
              Most Popular
            </span>
          </div>
          
          <div class="text-center flex-grow flex flex-col justify-between">
            <div>
              <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Professional</h3>
              <p class="text-text-secondary mb-8 font-brand">Ideal for growing businesses and teams</p>
              
              <div class="mb-10 transform transition-all duration-300 hover:scale-105">
                <span class="text-6xl font-brand font-brand-bold text-accent animate-number-counter">
                  ${{ isYearly ? '24' : '30' }}
                </span>
                <span class="text-text-secondary font-brand">{{ isYearly ? '/month' : '/month' }}</span>
                <div v-if="isYearly" class="text-sm text-accent font-brand-medium mt-2 animate-slide-in-left">
                  Billed annually ($288/year)
                </div>
              </div>
            </div>

            <ul class="space-y-5 mb-10 text-left">
              <li 
                v-for="(feature, index) in professionalFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.8 + index * 0.1}s` }"
              >
                <svg class="w-5 h-5 text-accent mr-3 flex-shrink-0 transform transition-transform duration-300 hover:scale-110" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                </svg>
                <span class="text-text-secondary font-brand">{{ feature }}</span>
              </li>
            </ul>

            <button class="w-full bg-gradient-to-r from-accent to-accent hover:opacity-90 text-primary font-brand font-brand-bold py-5 px-6 rounded-xl transition-all duration-300 hover:scale-105 shadow-lg hover:shadow-xl transform animate-gradient-shift">
              Start Free Trial
            </button>
          </div>
        </div>

        <!-- Enterprise Plan -->
        <div 
          class="relative bg-primary rounded-3xl shadow-xl border border-border p-8 transition-all duration-700 ease-out hover:shadow-2xl hover:-translate-y-2 opacity-0 translate-y-8 animate-fade-in-up"
          :style="{ animationDelay: '0.7s' }"
        >
          <div class="text-center">
            <h3 class="text-2xl font-brand font-brand-bold text-text-primary mb-2">Enterprise</h3>
            <p class="text-text-secondary mb-6 font-brand">Advanced features for large organizations</p>
            
            <div class="mb-8 transform transition-all duration-300 hover:scale-105">
              <span class="text-5xl font-brand font-brand-bold text-text-primary">
                ${{ isYearly ? '80' : '100' }}
              </span>
              <span class="text-text-secondary font-brand">{{ isYearly ? '/month' : '/month' }}</span>
              <div v-if="isYearly" class="text-sm text-accent font-brand-medium mt-1 animate-slide-in-left">
                Billed annually ($960/year)
              </div>
            </div>

            <ul class="space-y-4 mb-8 text-left">
              <li 
                v-for="(feature, index) in enterpriseFeatures" 
                :key="index"
                class="flex items-center opacity-0 translate-x-4 animate-slide-in-right"
                :style="{ animationDelay: `${0.9 + index * 0.1}s` }"
              >
                <svg class="w-5 h-5 text-accent mr-3 flex-shrink-0 transform transition-transform duration-300 hover:scale-110" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                </svg>
                <span class="text-text-secondary font-brand">{{ feature }}</span>
              </li>
            </ul>

            <button class="w-full bg-dark hover:bg-darker text-primary font-brand font-brand-semibold py-4 px-6 rounded-xl transition-all duration-300 hover:scale-105 transform hover:shadow-lg">
              Contact Sales
            </button>
          </div>
        </div>
      </div>

      <!-- FAQ Section -->
      <div 
        class="mt-24 text-center opacity-0 translate-y-8 animate-fade-in-up"
        :style="{ animationDelay: '1.2s' }"
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
            class="bg-primary rounded-2xl shadow-lg border border-border overflow-hidden opacity-0 translate-y-4 animate-fade-in-up transform transition-all duration-500 ease-out hover:scale-[1.02]"
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
import { ref, onMounted } from 'vue'

const isYearly = ref(false)
const openFAQ = ref(null)

const starterFeatures = [
  'Up to 5 projects',
  '10GB storage',
  'Email support',
  'Basic analytics'
]

const professionalFeatures = [
  'Unlimited projects',
  '100GB storage',
  'Priority support',
  'Advanced analytics',
  'Team collaboration'
]

const enterpriseFeatures = [
  'Everything in Professional',
  'Unlimited storage',
  '24/7 phone support',
  'Custom integrations',
  'Dedicated account manager'
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

onMounted(() => {
  // Trigger animations on mount
  const animatedElements = document.querySelectorAll('[class*="animate-"]')
  animatedElements.forEach(el => {
    el.style.animationFillMode = 'forwards'
  })
})
</script>

<style scoped>
@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(2rem);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in-right {
  from {
    opacity: 0;
    transform: translateX(1rem);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-in-left {
  from {
    opacity: 0;
    transform: translateX(-1rem);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes bounce-slow {
  0%, 100% {
    transform: translateY(0) translateX(-50%);
  }
  50% {
    transform: translateY(-5px) translateX(-50%);
  }
}

@keyframes glow {
  0%, 100% {
    box-shadow: 0 0 5px rgba(var(--accent), 0.5);
  }
  50% {
    box-shadow: 0 0 20px rgba(var(--accent), 0.8);
  }
}

@keyframes number-counter {
  from {
    opacity: 0;
    transform: scale(0.8);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes gradient-shift {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out both;
}

.animate-slide-in-right {
  animation: slide-in-right 0.7s ease-out both;
}

.animate-slide-in-left {
  animation: slide-in-left 0.7s ease-out both;
}

.animate-bounce-slow {
  animation: bounce-slow 3s ease-in-out infinite;
}

.animate-glow {
  animation: glow 2s ease-in-out infinite;
}

.animate-number-counter {
  animation: number-counter 1s ease-out both;
}

.animate-gradient-shift {
  background-size: 200% 200%;
  animation: gradient-shift 3s ease infinite;
}

/* Scroll-triggered animations */
@media (prefers-reduced-motion: no-preference) {
  .animate-on-scroll {
    opacity: 0;
    transform: translateY(2rem);
    transition: all 0.8s ease-out;
  }
  
  .animate-on-scroll.in-view {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Enhanced hover effects */
.hover-lift {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}
</style>