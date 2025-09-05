<template>
  <div class="min-h-screen bg-primary font-brand relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 pointer-events-none">
      <svg class="absolute w-full h-full opacity-[0.02]" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <pattern id="squares" x="0" y="0" width="80" height="80" patternUnits="userSpaceOnUse">
            <rect x="0" y="0" width="40" height="40" fill="none" stroke="currentColor" stroke-width="1" class="text-text-secondary"/>
            <rect x="40" y="40" width="40" height="40" fill="none" stroke="currentColor" stroke-width="1" class="text-text-secondary"/>
          </pattern>
        </defs>
        <rect x="0" y="0" width="100%" height="100%" fill="url(#squares)"/>
      </svg>
    </div>

    <!-- Content with relative positioning to stay above pattern -->
    <div class="relative z-10">
      <!-- Modern Hero Section -->
      <div class="bg-accentlight border-b border-border">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
          <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center mb-8">
            <div class="inline-flex items-center bg-primary border border-border rounded-full px-6 py-3 shadow-sm">
              <div class="w-2 h-2 bg-accent rounded-full mr-3"></div>
              <span class="text-text-secondary font-brand-medium">Support</span>
              <div class="w-2 h-2 bg-accent rounded-full ml-3"></div>
            </div>
          </div>

          <div class="text-center max-w-5xl mx-auto">
            <!-- Navigation Breadcrumb -->
            
            <h1 class="text-6xl md:text-7xl font-brand-bold mb-6 leading-none tracking-tight text-text-primary">
              Support Center
            </h1>
            <p class="text-2xl text-text-secondary mb-10 leading-relaxed font-light max-w-4xl mx-auto">
              Get expert help through multiple channels. Our dedicated support team and comprehensive resources are here to ensure your success.
            </p>
            
            <!-- Stats Bar -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
              <div class="bg-primary border border-border rounded-2xl p-6">
                <div class="text-3xl font-brand-bold text-accent mb-2">24/7</div>
                <div class="text-text-secondary">Support Available</div>
              </div>
              <div class="bg-primary border border-border rounded-2xl p-6">
                <div class="text-3xl font-brand-bold text-accent mb-2">&lt;30s</div>
                <div class="text-text-secondary">Average Response</div>
              </div>
              <div class="bg-primary border border-border rounded-2xl p-6">
                <div class="text-3xl font-brand-bold text-accent mb-2">99.8%</div>
                <div class="text-text-secondary">Uptime Guarantee</div>
              </div>
            </div>
            
            <!-- Contact Buttons -->
            <div class="flex flex-col md:flex-row gap-6 justify-center items-center max-w-2xl mx-auto">
              <button @click="handleEmailContact" class="group w-full md:w-auto bg-accent hover:bg-accent/90 text-primary px-10 py-4 rounded-xl font-brand-semibold text-lg transition-all duration-300 flex items-center justify-center space-x-3 shadow-lg hover:shadow-xl hover:scale-105">
                <svg class="w-5 h-5 group-hover:rotate-12 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                </svg>
                <span>Contact via Email</span>
              </button>
              
              <button @click="handlePhoneContact" class="group w-full md:w-auto bg-transparent border-2 border-accent hover:border-accent hover:bg-accent/5 text-accent px-10 py-4 rounded-xl font-brand-semibold text-lg transition-all duration-300 flex items-center justify-center space-x-3">
                <svg class="w-5 h-5 group-hover:rotate-12 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                </svg>
                <span>Contact via Phone</span>
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Modern Support Grid -->
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <div class="text-center mb-20">
          <h2 class="text-5xl font-brand-bold text-text-primary mb-6 tracking-tight">How we can help</h2>
          <p class="text-2xl text-text-secondary font-light max-w-4xl mx-auto">Choose the support option that fits your needs and timeline</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-20">
          <!-- Live Chat - Featured -->
          <div class="group bg-accentlight border-2 border-accent/20 hover:border-accent rounded-3xl p-12 transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 relative overflow-hidden">
            <div class="absolute top-8 right-8 bg-accent text-primary px-4 py-2 rounded-full text-sm font-brand-semibold">
              INSTANT
            </div>
            <div class="w-20 h-20 bg-accent rounded-3xl flex items-center justify-center mb-8 group-hover:scale-110 transition-transform duration-300">
              <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
              </svg>
            </div>
            <h3 class="text-3xl font-brand-bold text-text-primary mb-6">Live Chat Support</h3>
            <p class="text-lg text-text-secondary mb-8 leading-relaxed">Connect instantly with our support specialists. Get real-time answers to your questions and immediate assistance with any technical issues.</p>
            
            <div class="flex items-center space-x-6 mb-8">
              <div class="flex items-center space-x-3">
                <div class="w-3 h-3 bg-green-500 rounded-full animate-pulse"></div>
                <span class="font-brand-semibold text-text-primary">Online now</span>
              </div>
              <div class="text-text-muted">•</div>
              <span class="text-text-muted">Average response: 30 seconds</span>
            </div>
            
            <button class="w-full bg-accent text-primary py-5 rounded-2xl font-brand-bold text-lg hover:bg-accent/90 transition-colors shadow-lg">
              Start Live Chat
            </button>
          </div>

          <!-- Knowledge Base - Featured -->
          <div class="group bg-primary border-2 border-border hover:border-accent/30 rounded-3xl p-12 transition-all duration-500 hover:shadow-2xl hover:-translate-y-2">
            <div class="w-20 h-20 bg-navlink rounded-3xl flex items-center justify-center mb-8 group-hover:scale-110 transition-transform duration-300">
              <svg class="w-10 h-10 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"></path>
              </svg>
            </div>
            <h3 class="text-3xl font-brand-bold text-text-primary mb-6">Help Center</h3>
            <p class="text-lg text-text-secondary mb-8 leading-relaxed">Browse our comprehensive documentation, step-by-step guides, and detailed tutorials. Find in-depth answers to complex questions.</p>
            
            <div class="flex items-center space-x-6 mb-8">
              <span class="font-brand-semibold text-text-primary">500+ articles</span>
              <div class="text-text-muted">•</div>
              <span class="text-text-muted">Searchable content</span>
            </div>
            
            <button class="w-full bg-navlink text-primary py-5 rounded-2xl font-brand-bold text-lg hover:bg-navlink/90 transition-colors shadow-lg">
              Browse Help Center
            </button>
          </div>
        </div>

        <!-- Secondary Options -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="group bg-primary border border-border hover:border-accent/30 rounded-2xl p-8 transition-all duration-300 hover:shadow-xl">
            <div class="w-16 h-16 bg-accentlight rounded-2xl flex items-center justify-center mb-6 group-hover:scale-105 transition-transform">
              <svg class="w-8 h-8 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path>
              </svg>
            </div>
            <h4 class="text-xl font-brand-bold text-text-primary mb-4">Community</h4>
            <p class="text-text-secondary mb-6">Connect with other users and learn from shared experiences</p>
            <button class="text-accent font-brand-semibold hover:text-accent/80 transition-colors">
              Join Community →
            </button>
          </div>

          <div class="group bg-primary border border-border hover:border-accent/30 rounded-2xl p-8 transition-all duration-300 hover:shadow-xl">
            <div class="w-16 h-16 bg-accentlight rounded-2xl flex items-center justify-center mb-6 group-hover:scale-105 transition-transform">
              <svg class="w-8 h-8 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h1m4 0h1M9 16h1m4 0h1"></path>
              </svg>
            </div>
            <h4 class="text-xl font-brand-bold text-text-primary mb-4">Video Guides</h4>
            <p class="text-text-secondary mb-6">Watch step-by-step tutorials and feature demonstrations</p>
            <button class="text-accent font-brand-semibold hover:text-accent/80 transition-colors">
              Watch Videos →
            </button>
          </div>

          <div class="group bg-primary border border-border hover:border-accent/30 rounded-2xl p-8 transition-all duration-300 hover:shadow-xl">
            <div class="w-16 h-16 bg-accentlight rounded-2xl flex items-center justify-center mb-6 group-hover:scale-105 transition-transform">
              <svg class="w-8 h-8 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v4a2 2 0 01-2 2h-2a2 2 0 00-2-2z"></path>
              </svg>
            </div>
            <h4 class="text-xl font-brand-bold text-text-primary mb-4">System Status</h4>
            <p class="text-text-secondary mb-6">Check current system performance and service updates</p>
            <button class="text-accent font-brand-semibold hover:text-accent/80 transition-colors">
              View Status →
            </button>
          </div>
        </div>
      </div>

      <!-- FAQ Section -->
      <div class="bg-accentlight py-24">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center mb-16">
            <h2 class="text-4xl font-brand-bold text-text-primary mb-6">Frequently Asked Questions</h2>
            <p class="text-xl text-text-secondary">Quick answers to the most common questions</p>
          </div>

          <div class="space-y-6">
            <div class="bg-primary border border-border rounded-2xl overflow-hidden">
              <button @click="toggleFaq(1)" class="w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors">
                <h3 class="text-lg font-brand-semibold text-text-primary">How quickly can I expect a response to my support request?</h3>
                <svg :class="{ 'rotate-180': openFaq === 1 }" class="w-5 h-5 text-text-secondary transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 1" class="px-8 pb-6">
                <p class="text-text-secondary leading-relaxed">Our response times depend on the support channel you choose. Live chat typically receives responses within 30 seconds, email support within 2-4 hours during business hours, and phone support is available for immediate assistance during business hours (9 AM - 6 PM EST).</p>
              </div>
            </div>

            <div class="bg-primary border border-border rounded-2xl overflow-hidden">
              <button @click="toggleFaq(2)" class="w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors">
                <h3 class="text-lg font-brand-semibold text-text-primary">What information should I include when contacting support?</h3>
                <svg :class="{ 'rotate-180': openFaq === 2 }" class="w-5 h-5 text-text-secondary transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 2" class="px-8 pb-6">
                <p class="text-text-secondary leading-relaxed">To help us assist you quickly, please include: your account email, a detailed description of the issue, any error messages you're seeing, steps you've already tried, and screenshots if relevant. The more context you provide, the faster we can resolve your issue.</p>
              </div>
            </div>

            <div class="bg-primary border border-border rounded-2xl overflow-hidden">
              <button @click="toggleFaq(3)" class="w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors">
                <h3 class="text-lg font-brand-semibold text-text-primary">Is support available 24/7?</h3>
                <svg :class="{ 'rotate-180': openFaq === 3 }" class="w-5 h-5 text-text-secondary transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 3" class="px-8 pb-6">
                <p class="text-text-secondary leading-relaxed">Yes! Our live chat and email support are available 24/7. Phone support is available during business hours (9 AM - 6 PM EST, Monday-Friday). For urgent issues outside business hours, we recommend using live chat for the fastest response.</p>
              </div>
            </div>

            <div class="bg-primary border border-border rounded-2xl overflow-hidden">
              <button @click="toggleFaq(4)" class="w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors">
                <h3 class="text-lg font-brand-semibold text-text-primary">Do you offer phone support for all users?</h3>
                <svg :class="{ 'rotate-180': openFaq === 4 }" class="w-5 h-5 text-text-secondary transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 4" class="px-8 pb-6">
                <p class="text-text-secondary leading-relaxed">Phone support is available for all paid plan users. Free plan users have access to live chat, email support, and our comprehensive help center. You can upgrade to any paid plan to access phone support and priority assistance.</p>
              </div>
            </div>

            <div class="bg-primary border border-border rounded-2xl overflow-hidden">
              <button @click="toggleFaq(5)" class="w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors">
                <h3 class="text-lg font-brand-semibold text-text-primary">Can I schedule a call with your support team?</h3>
                <svg :class="{ 'rotate-180': openFaq === 5 }" class="w-5 h-5 text-text-secondary transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 5" class="px-8 pb-6">
                <p class="text-text-secondary leading-relaxed">Absolutely! Premium plan users can schedule one-on-one calls with our technical specialists. You can book these sessions through your account dashboard or by contacting our support team. Standard plan users can request scheduled calls for complex technical issues.</p>
              </div>
            </div>

            <div class="bg-primary border border-border rounded-2xl overflow-hidden">
              <button @click="toggleFaq(6)" class="w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors">
                <h3 class="text-lg font-brand-semibold text-text-primary">Where can I find troubleshooting guides?</h3>
                <svg :class="{ 'rotate-180': openFaq === 6 }" class="w-5 h-5 text-text-secondary transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </button>
              <div v-show="openFaq === 6" class="px-8 pb-6">
                <p class="text-text-secondary leading-relaxed">Our comprehensive help center contains over 500 articles, including detailed troubleshooting guides, step-by-step tutorials, and video walkthroughs. You can access it by clicking "Browse Help Center" above, or use the search function to find specific topics.</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Contact Hours -->
      <div class="bg-primary py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
            <div class="bg-accentlight rounded-2xl p-8">
              <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center mx-auto mb-4">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                </svg>
              </div>
              <h3 class="text-xl font-brand-semibold text-text-primary mb-2">Live Chat</h3>
              <p class="text-text-secondary">Available 24/7</p>
            </div>

            <div class="bg-accentlight rounded-2xl p-8">
              <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center mx-auto mb-4">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                </svg>
              </div>
              <h3 class="text-xl font-brand-semibold text-text-primary mb-2">Email Support</h3>
              <p class="text-text-secondary">Available 24/7</p>
            </div>

            <div class="bg-accentlight rounded-2xl p-8">
              <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center mx-auto mb-4">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                </svg>
              </div>
              <h3 class="text-xl font-brand-semibold text-text-primary mb-2">Phone Support</h3>
              <p class="text-text-secondary">Mon-Fri, 9 AM - 6 PM EST</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Final CTA - Changed from black to accentlight -->
      <div class="bg-accentlight py-20 mb-12">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
          <h2 class="text-4xl font-brand-bold text-text-primary mb-6">Ready to get started?</h2>
          <p class="text-xl text-text-secondary mb-10 max-w-3xl mx-auto leading-relaxed">
            Our support team is standing by to help you succeed. Choose your preferred method and get the assistance you need.
          </p>
          
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <button class="bg-accent text-primary px-8 py-4 rounded-xl font-brand-semibold text-lg hover:bg-accent/90 transition-all duration-300 shadow-lg hover:scale-105">
              Start Live Chat
            </button>
            <button class="border-2 border-accent text-accent px-8 py-4 rounded-xl font-brand-semibold text-lg hover:bg-accent/5 transition-colors">
              Browse Help Center
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// SEO Meta
useSeoMeta({
  title: 'Support Center - Professional Help and Documentation',
  description: 'Get expert support through live chat, comprehensive documentation, phone support, and community resources. Available 24/7.',
})

// FAQ functionality
const openFaq = ref(null)

const toggleFaq = (id) => {
  openFaq.value = openFaq.value === id ? null : id
}

// Handler functions
const handleEmailContact = () => {
  // Navigate to email contact form or open mailto
  window.location.href = 'mailto:support@yourcompany.com'
}

const handlePhoneContact = () => {
  // Navigate to phone contact page or show phone number
  window.location.href = 'tel:+1-800-123-4567'
}

const handleSupportOption = (option) => {
  switch(option) {
    case 'chat':
      // Initialize chat widget
      break
    case 'help-center':
      navigateTo('/help')
      break
    case 'community':
      navigateTo('/community')
      break
    case 'videos':
      navigateTo('/help/videos')
      break
    case 'status':
      navigateTo('/status')
      break
  }
}
</script>
