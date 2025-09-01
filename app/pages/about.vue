<template>
  <div class="min-h-screen bg-white font-brand">
    
    <!-- Modern Hero Section -->
    <section class="relative py-24 lg:py-32 px-4 sm:px-6 lg:px-8 bg-white overflow-hidden" ref="heroRef">
      <!-- Simplified Background -->
      <div class="absolute inset-0 overflow-hidden">
        <!-- Grid Pattern Background -->
        <div class="absolute inset-0 bg-[linear-gradient(to_right,#f0f0f0_1px,transparent_1px),linear-gradient(to_bottom,#f0f0f0_1px,transparent_1px)] bg-[size:6rem_4rem]"></div>
        
        <!-- Subtle Lines -->
        <div class="absolute top-0 left-1/4 w-px h-full bg-gradient-to-b from-transparent via-accent/20 to-transparent"></div>
        <div class="absolute top-0 right-1/3 w-px h-full bg-gradient-to-b from-transparent via-purple-500/20 to-transparent"></div>
        
        <!-- Animated Orbs -->
        <div class="absolute top-20 left-10 w-64 h-64 bg-gradient-radial from-accent/20 via-purple-300/10 to-transparent rounded-full blur-3xl animate-float"></div>
        <div class="absolute bottom-20 right-10 w-96 h-96 bg-gradient-radial from-purple-500/20 via-accent/10 to-transparent rounded-full blur-3xl animate-float-delayed"></div>
      </div>
      
      <div class="max-w-7xl mx-auto relative z-10">
        <div class="text-center">
          <!-- Clean Badge -->
          <div class="inline-flex items-center gap-3 bg-white shadow-lg backdrop-blur-sm rounded-full px-8 py-4 mb-10 border border-gray-200 transform transition-all duration-700 ease-out"
               :class="heroVisible ? 'opacity-100 translate-y-0 scale-100' : 'opacity-0 translate-y-8 scale-95'">
            <div class="w-2 h-2 bg-accent rounded-full animate-pulse"></div>
            <span class="text-text-primary font-brand-medium text-sm tracking-wide">About Station List Pro</span>
            <div class="w-2 h-2 bg-accent rounded-full animate-pulse"></div>
          </div>
          
          <!-- Main heading -->
          <h1 class="text-5xl md:text-6xl lg:text-8xl font-brand-bold text-text-primary mb-8 leading-tight transform transition-all duration-700 ease-out delay-200"
              :class="heroVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
            Revolutionizing
            <span class="relative inline-block">
              <span class="text-accent animate-text-shimmer bg-gradient-to-r from-accent via-purple-600 to-accent bg-[length:200%_100%] bg-clip-text text-transparent">
                Station Management
              </span>
              <div class="absolute -bottom-2 left-0 right-0 h-1 bg-gradient-to-r from-accent to-purple-600 rounded-full transform scale-x-0 transition-transform duration-700 delay-1000"
                   :class="heroVisible ? 'scale-x-100' : 'scale-x-0'"></div>
            </span>
          </h1>
          
          <!-- Subtitle -->
          <p class="max-w-4xl mx-auto text-xl md:text-2xl text-text-secondary leading-relaxed mb-12 font-brand transform transition-all duration-700 ease-out delay-300"
             :class="heroVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
            <span class="font-brand-semibold text-text-primary">Station List Pro</span> empowers businesses with intelligent station management solutions. Our cutting-edge platform combines innovation with reliability to deliver unprecedented operational efficiency.
          </p>
          
          <!-- CTA Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 justify-center transform transition-all duration-700 ease-out delay-400"
               :class="heroVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
            <button class="group bg-accent hover:bg-purple-700 text-white font-brand-semibold px-10 py-5 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105 hover:-translate-y-2 inline-flex items-center gap-3">
              <span>Discover Our Platform</span>
              <svg class="w-5 h-5 transition-transform duration-200 group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
              </svg>
            </button>
            <button class="group bg-white hover:bg-gray-50 text-accent border-2 border-gray-200 hover:border-accent font-brand-semibold px-10 py-5 rounded-2xl shadow-lg transition-all duration-300 transform hover:scale-105 hover:-translate-y-2 inline-flex items-center gap-3">
              <span>Watch Demo</span>
              <svg class="w-5 h-5 transition-transform duration-200 group-hover:scale-110" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h1m4 0h1m-6 4h.01M19 10a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Mission Section with Real Image -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-white" ref="missionRef">
      <div class="max-w-7xl mx-auto">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-20 items-center">
          <!-- Content -->
          <div class="transform transition-all duration-700 ease-out"
               :class="missionVisible ? 'opacity-100 translate-x-0' : 'opacity-0 -translate-x-12'">
            <div class="inline-flex items-center gap-2 bg-accentlight rounded-full px-6 py-3 mb-8 animate-bounce-subtle">
              <svg class="w-4 h-4 text-accent animate-spin-slow" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
              </svg>
              <span class="text-accent font-brand-medium text-sm">Our Mission</span>
            </div>
            <h2 class="text-4xl md:text-5xl lg:text-6xl font-brand-bold text-text-primary mb-8 leading-tight">
              Transforming Station Operations
              <span class="text-accent bg-gradient-to-r from-accent to-purple-600 bg-clip-text text-transparent animate-text-shimmer bg-[length:200%_100%]">Worldwide</span>
            </h2>
            <div class="space-y-6">
              <p class="text-xl text-text-secondary leading-relaxed font-brand transform transition-all duration-500 delay-100"
                 :class="missionVisible ? 'opacity-100 translate-x-0' : 'opacity-0 -translate-x-4'">
                At <span class="font-brand-semibold text-text-primary">Station List Pro</span>, we're dedicated to revolutionizing how stations are managed, monitored, and optimized across industries.
              </p>
              <p class="text-lg text-text-secondary leading-relaxed font-brand transform transition-all duration-500 delay-200"
                 :class="missionVisible ? 'opacity-100 translate-x-0' : 'opacity-0 -translate-x-4'">
                Our advanced platform integrates seamlessly with existing infrastructure, providing real-time insights, automated workflows, and predictive analytics that drive operational excellence.
              </p>
              <p class="text-lg text-text-secondary leading-relaxed font-brand transform transition-all duration-500 delay-300"
                 :class="missionVisible ? 'opacity-100 translate-x-0' : 'opacity-0 -translate-x-4'">
                Since 2020, we've empowered over <span class="font-brand-semibold text-accent">15,000+ organizations</span> to achieve remarkable efficiency gains and cost reductions through intelligent station management.
              </p>
            </div>
            
            <!-- Stats -->
            <div class="grid grid-cols-3 gap-8 mt-12 p-8 bg-gradient-to-r from-accentlight to-white rounded-2xl border border-accent/10 hover:shadow-xl transition-all duration-500 transform hover:scale-105"
                 :class="missionVisible ? 'opacity-100 translate-x-0' : 'opacity-0 -translate-x-8'"
                 style="transition-delay: 400ms;">
              <div class="text-center">
                <div class="text-3xl font-brand-bold text-accent mb-2">15K+</div>
                <div class="text-text-secondary font-brand-medium text-sm">Active Stations</div>
              </div>
              <div class="text-center">
                <div class="text-3xl font-brand-bold text-accent mb-2">99.9%</div>
                <div class="text-text-secondary font-brand-medium text-sm">Uptime</div>
              </div>
              <div class="text-center">
                <div class="text-3xl font-brand-bold text-accent mb-2">24/7</div>
                <div class="text-text-secondary font-brand-medium text-sm">Support</div>
              </div>
            </div>
          </div>
          
          <!-- Real Image -->
          <div class="transform transition-all duration-700 ease-out delay-200"
               :class="missionVisible ? 'opacity-100 translate-x-0' : 'opacity-0 translate-x-12'">
            <div class="relative group">
              <img src="https://cdn.pixabay.com/photo/2023/05/18/19/08/buildings-8003075_1280.jpg" 
                   alt="Modern office with technology" 
                   class="w-full h-full object-cover rounded-3xl shadow-2xl transition-all duration-500 group-hover:scale-105 group-hover:shadow-3xl">
              <!-- Decorative elements -->
              <div class="absolute -bottom-8 -right-8 w-32 h-32 bg-accent/20 rounded-3xl blur-sm animate-float"></div>
              <div class="absolute -top-8 -left-8 w-24 h-24 bg-accent/10 rounded-2xl blur-sm animate-float-delayed"></div>
              
              <!-- Overlay effect on hover -->
              <div class="absolute inset-0 bg-gradient-to-tr from-accent/0 to-purple-600/0 group-hover:from-accent/10 group-hover:to-purple-600/10 rounded-3xl transition-all duration-500"></div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section - Enhanced -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-50 relative overflow-hidden" ref="teamRef">
      <!-- Background Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-0 left-0 w-72 h-72 bg-accent/10 rounded-full blur-3xl animate-float"></div>
        <div class="absolute bottom-0 right-0 w-96 h-96 bg-purple-500/10 rounded-full blur-3xl animate-float-delayed"></div>
      </div>
      
      <div class="max-w-7xl mx-auto relative z-10">
        <!-- Section Header -->
        <div class="text-center mb-20 transform transition-all duration-700 ease-out"
             :class="teamVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <div class="inline-flex items-center gap-2 bg-white rounded-full px-6 py-3 mb-8 shadow-lg border border-accent/10">
            <svg class="w-4 h-4 text-accent animate-pulse" fill="currentColor" viewBox="0 0 20 20">
              <path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3z"/>
            </svg>
            <span class="text-accent font-brand-medium text-sm">Leadership Team</span>
          </div>
          <h2 class="text-4xl md:text-5xl lg:text-6xl font-brand-bold text-text-primary mb-6">
            The Visionaries Behind
            <span class="text-accent bg-gradient-to-r from-accent to-purple-600 bg-clip-text text-transparent animate-text-shimmer bg-[length:200%_100%]">Station List Pro</span>
          </h2>
          <p class="max-w-3xl mx-auto text-xl text-text-secondary font-brand leading-relaxed">
            Our leadership team combines decades of industry expertise with innovative thinking to drive the future of station management technology.
          </p>
        </div>

        <!-- Team Grid - Enhanced -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
          <!-- Team Member 1 -->
          <div class="group bg-white rounded-3xl p-10 shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-3 hover:scale-105 border border-gray-100 hover:border-accent/20 relative overflow-hidden"
               :class="teamVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: teamVisible ? '200ms' : '0ms' }">
            <!-- Hover Background Effect -->
            <div class="absolute inset-0 bg-gradient-to-br from-accent/5 to-purple-600/5 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="text-center relative z-10">
              <div class="w-28 h-28 bg-gradient-to-br from-accent to-purple-600 rounded-2xl mx-auto mb-8 flex items-center justify-center group-hover:scale-110 transition-transform duration-300 shadow-lg relative overflow-hidden">
                <span class="text-white font-brand-bold text-3xl relative z-10">JS</span>
                <div class="absolute inset-0 bg-gradient-to-br from-white/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </div>
              <h3 class="text-2xl font-brand-bold text-text-primary mb-3 group-hover:text-accent transition-colors duration-300">John Smith</h3>
              <p class="text-accent font-brand-semibold mb-2">CEO & Founder</p>
              <div class="w-12 h-0.5 bg-accent mx-auto mb-4 transform scale-x-50 group-hover:scale-x-100 transition-transform duration-300"></div>
              <p class="text-text-secondary leading-relaxed font-brand">
                Visionary leader with 15+ years of experience in scaling tech companies. Expert in station management systems and digital transformation.
              </p>
            </div>
          </div>

          <!-- Team Member 2 -->
          <div class="group bg-white rounded-3xl p-10 shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-3 hover:scale-105 border border-gray-100 hover:border-accent/20 relative overflow-hidden"
               :class="teamVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: teamVisible ? '400ms' : '0ms' }">
            <!-- Hover Background Effect -->
            <div class="absolute inset-0 bg-gradient-to-br from-accent/5 to-purple-600/5 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="text-center relative z-10">
              <div class="w-28 h-28 bg-gradient-to-br from-accent to-purple-600 rounded-2xl mx-auto mb-8 flex items-center justify-center group-hover:scale-110 transition-transform duration-300 shadow-lg relative overflow-hidden">
                <span class="text-white font-brand-bold text-3xl relative z-10">SJ</span>
                <div class="absolute inset-0 bg-gradient-to-br from-white/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </div>
              <h3 class="text-2xl font-brand-bold text-text-primary mb-3 group-hover:text-accent transition-colors duration-300">Sarah Johnson</h3>
              <p class="text-accent font-brand-semibold mb-2">Chief Technology Officer</p>
              <div class="w-12 h-0.5 bg-accent mx-auto mb-4 transform scale-x-50 group-hover:scale-x-100 transition-transform duration-300"></div>
              <p class="text-text-secondary leading-relaxed font-brand">
                Technical architect and engineering leader passionate about building scalable, secure, and innovative station management solutions.
              </p>
            </div>
          </div>

          <!-- Team Member 3 -->
          <div class="group bg-white rounded-3xl p-10 shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-3 hover:scale-105 border border-gray-100 hover:border-accent/20 relative overflow-hidden"
               :class="teamVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: teamVisible ? '600ms' : '0ms' }">
            <!-- Hover Background Effect -->
            <div class="absolute inset-0 bg-gradient-to-br from-accent/5 to-purple-600/5 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="text-center relative z-10">
              <div class="w-28 h-28 bg-gradient-to-br from-accent to-purple-600 rounded-2xl mx-auto mb-8 flex items-center justify-center group-hover:scale-110 transition-transform duration-300 shadow-lg relative overflow-hidden">
                <span class="text-white font-brand-bold text-3xl relative z-10">MB</span>
                <div class="absolute inset-0 bg-gradient-to-br from-white/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </div>
              <h3 class="text-2xl font-brand-bold text-text-primary mb-3 group-hover:text-accent transition-colors duration-300">Mike Brown</h3>
              <p class="text-accent font-brand-semibold mb-2">Head of Product Design</p>
              <div class="w-12 h-0.5 bg-accent mx-auto mb-4 transform scale-x-50 group-hover:scale-x-100 transition-transform duration-300"></div>
              <p class="text-text-secondary leading-relaxed font-brand">
                Creative design leader focused on crafting intuitive user experiences and beautiful, functional interfaces for complex systems.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Values Section - Enhanced -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-white relative overflow-hidden" ref="valuesRef">
      <!-- Background Pattern -->
      <div class="absolute inset-0">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_50%_50%,rgba(99,102,241,0.05),transparent)] opacity-50"></div>
      </div>
      
      <div class="max-w-7xl mx-auto relative z-10">
        <!-- Section Header -->
        <div class="text-center mb-20 transform transition-all duration-700 ease-out"
             :class="valuesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <div class="inline-flex items-center gap-2 bg-accentlight rounded-full px-6 py-3 mb-8 animate-bounce-subtle">
            <svg class="w-4 h-4 text-accent animate-spin-slow" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M3 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm0 4a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"/>
            </svg>
            <span class="text-accent font-brand-medium text-sm">Core Values</span>
          </div>
          <h2 class="text-4xl md:text-5xl lg:text-6xl font-brand-bold text-text-primary mb-6">
            What Drives <span class="text-accent bg-gradient-to-r from-accent to-purple-600 bg-clip-text text-transparent animate-text-shimmer bg-[length:200%_100%]">Station List Pro</span>
          </h2>
          <p class="max-w-3xl mx-auto text-xl text-text-secondary font-brand leading-relaxed">
            These fundamental principles guide every decision we make and shape how we serve our clients worldwide.
          </p>
        </div>

        <!-- Values Grid - Enhanced -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
          <!-- Value 1 -->
          <div class="group text-center p-10 rounded-3xl border border-gray-100 hover:border-accent/30 hover:shadow-xl transition-all duration-500 transform hover:-translate-y-2 bg-gradient-to-b from-white to-gray-50/50 relative overflow-hidden"
               :class="valuesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: valuesVisible ? '200ms' : '0ms' }">
            <!-- Hover Effect -->
            <div class="absolute inset-0 bg-gradient-to-br from-accent/10 to-purple-600/5 opacity-0 group-hover:opacity-100 transition-all duration-500 rounded-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-20 h-20 bg-gradient-to-br from-accent to-purple-600 rounded-3xl mx-auto mb-8 flex items-center justify-center group-hover:scale-110 transition-all duration-300 shadow-lg relative overflow-hidden">
                <svg class="w-10 h-10 text-white relative z-10 group-hover:rotate-12 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                </svg>
                <div class="absolute inset-0 bg-white/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </div>
              <h3 class="text-2xl font-brand-bold text-text-primary mb-6 group-hover:text-accent transition-colors duration-300">Innovation Excellence</h3>
              <p class="text-text-secondary font-brand leading-relaxed text-lg">
                We continuously push technological boundaries to deliver cutting-edge station management solutions that drive measurable results.
              </p>
            </div>
          </div>

          <!-- Value 2 -->
          <div class="group text-center p-10 rounded-3xl border border-gray-100 hover:border-accent/30 hover:shadow-xl transition-all duration-500 transform hover:-translate-y-2 bg-gradient-to-b from-white to-gray-50/50 relative overflow-hidden"
               :class="valuesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: valuesVisible ? '400ms' : '0ms' }">
            <!-- Hover Effect -->
            <div class="absolute inset-0 bg-gradient-to-br from-accent/10 to-purple-600/5 opacity-0 group-hover:opacity-100 transition-all duration-500 rounded-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-20 h-20 bg-gradient-to-br from-accent to-purple-600 rounded-3xl mx-auto mb-8 flex items-center justify-center group-hover:scale-110 transition-all duration-300 shadow-lg relative overflow-hidden">
                <svg class="w-10 h-10 text-white relative z-10 group-hover:rotate-12 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/>
                </svg>
                <div class="absolute inset-0 bg-white/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </div>
              <h3 class="text-2xl font-brand-bold text-text-primary mb-6 group-hover:text-accent transition-colors duration-300">Client Success Focus</h3>
              <p class="text-text-secondary font-brand leading-relaxed text-lg">
                Our clients' operational success is our primary measure of achievement. We build lasting partnerships through exceptional service delivery.
              </p>
            </div>
          </div>

          <!-- Value 3 -->
          <div class="group text-center p-10 rounded-3xl border border-gray-100 hover:border-accent/30 hover:shadow-xl transition-all duration-500 transform hover:-translate-y-2 bg-gradient-to-b from-white to-gray-50/50 relative overflow-hidden"
               :class="valuesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: valuesVisible ? '600ms' : '0ms' }">
            <!-- Hover Effect -->
            <div class="absolute inset-0 bg-gradient-to-br from-accent/10 to-purple-600/5 opacity-0 group-hover:opacity-100 transition-all duration-500 rounded-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-20 h-20 bg-gradient-to-br from-accent to-purple-600 rounded-3xl mx-auto mb-8 flex items-center justify-center group-hover:scale-110 transition-all duration-300 shadow-lg relative overflow-hidden">
                <svg class="w-10 h-10 text-white relative z-10 group-hover:rotate-12 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                </svg>
                <div class="absolute inset-0 bg-white/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </div>
              <h3 class="text-2xl font-brand-bold text-text-primary mb-6 group-hover:text-accent transition-colors duration-300">Quality Assurance</h3>
              <p class="text-text-secondary font-brand leading-relaxed text-lg">
                We maintain the highest industry standards in every aspect of our platform - from security to system reliability.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Enhanced Statistics Section with Counting Animation -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-gradient-to-r from-accent to-purple-700 relative overflow-hidden" ref="statsRef">
      <!-- Animated Background Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-0 left-0 w-96 h-96 bg-white/10 rounded-full blur-3xl animate-float"></div>
        <div class="absolute bottom-0 right-0 w-72 h-72 bg-purple-300/20 rounded-full blur-3xl animate-float-delayed"></div>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-white/5 rounded-full blur-2xl animate-pulse"></div>
      </div>
      
      <div class="max-w-7xl mx-auto relative z-10">
        <div class="text-center mb-16 transform transition-all duration-700 ease-out"
             :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <h2 class="text-4xl md:text-5xl font-brand-bold text-white mb-4 animate-text-shimmer bg-gradient-to-r from-white via-purple-200 to-white bg-[length:200%_100%] bg-clip-text text-transparent">
            Station List Pro by the Numbers
          </h2>
          <p class="text-xl text-purple-100 font-brand">Trusted by organizations worldwide</p>
        </div>
        
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
          <!-- Active Stations Counter -->
          <div class="group bg-white/10 backdrop-blur-sm rounded-2xl p-8 transform transition-all duration-700 ease-out hover:bg-white/15 hover:scale-105 border border-white/20 hover:border-white/40 relative overflow-hidden"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '100ms' : '0ms' }">
            <!-- Shimmer effect -->
            <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -translate-x-full animate-shimmer group-hover:translate-x-full transition-transform duration-1000"></div>
            
            <div class="text-5xl md:text-6xl font-brand-bold text-white mb-4 relative z-10">
              {{ animatedStats.activeStations }}K+
            </div>
            <p class="text-purple-100 font-brand-medium text-lg group-hover:text-white transition-colors duration-300">Active Stations</p>
            
            <!-- Floating icon -->
            <div class="absolute top-4 right-4 opacity-20 group-hover:opacity-40 transition-opacity duration-300">
              <svg class="w-6 h-6 text-white animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
              </svg>
            </div>
          </div>
          
          <!-- Team Experts Counter -->
          <div class="group bg-white/10 backdrop-blur-sm rounded-2xl p-8 transform transition-all duration-700 ease-out hover:bg-white/15 hover:scale-105 border border-white/20 hover:border-white/40 relative overflow-hidden"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '200ms' : '0ms' }">
            <!-- Shimmer effect -->
            <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -translate-x-full animate-shimmer group-hover:translate-x-full transition-transform duration-1000" style="animation-delay: 0.2s;"></div>
            
            <div class="text-5xl md:text-6xl font-brand-bold text-white mb-4 relative z-10">
              {{ animatedStats.teamExperts }}+
            </div>
            <p class="text-purple-100 font-brand-medium text-lg group-hover:text-white transition-colors duration-300">Team Experts</p>
            
            <!-- Floating icon -->
            <div class="absolute top-4 right-4 opacity-20 group-hover:opacity-40 transition-opacity duration-300">
              <svg class="w-6 h-6 text-white animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/>
              </svg>
            </div>
          </div>
          
          <!-- Projects Delivered Counter -->
          <div class="group bg-white/10 backdrop-blur-sm rounded-2xl p-8 transform transition-all duration-700 ease-out hover:bg-white/15 hover:scale-105 border border-white/20 hover:border-white/40 relative overflow-hidden"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '300ms' : '0ms' }">
            <!-- Shimmer effect -->
            <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -translate-x-full animate-shimmer group-hover:translate-x-full transition-transform duration-1000" style="animation-delay: 0.4s;"></div>
            
            <div class="text-5xl md:text-6xl font-brand-bold text-white mb-4 relative z-10">
              {{ animatedStats.projectsDelivered }}+
            </div>
            <p class="text-purple-100 font-brand-medium text-lg group-hover:text-white transition-colors duration-300">Projects Delivered</p>
            
            <!-- Floating icon -->
            <div class="absolute top-4 right-4 opacity-20 group-hover:opacity-40 transition-opacity duration-300">
              <svg class="w-6 h-6 text-white animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
          </div>
          
          <!-- Years Excellence Counter -->
          <div class="group bg-white/10 backdrop-blur-sm rounded-2xl p-8 transform transition-all duration-700 ease-out hover:bg-white/15 hover:scale-105 border border-white/20 hover:border-white/40 relative overflow-hidden"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '400ms' : '0ms' }">
            <!-- Shimmer effect -->
            <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -translate-x-full animate-shimmer group-hover:translate-x-full transition-transform duration-1000" style="animation-delay: 0.6s;"></div>
            
            <div class="text-5xl md:text-6xl font-brand-bold text-white mb-4 relative z-10">
              {{ animatedStats.yearsExcellence }}+
            </div>
            <p class="text-purple-100 font-brand-medium text-lg group-hover:text-white transition-colors duration-300">Years Excellence</p>
            
            <!-- Floating icon -->
            <div class="absolute top-4 right-4 opacity-20 group-hover:opacity-40 transition-opacity duration-300">
              <svg class="w-6 h-6 text-white animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Enhanced CTA Section -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-accentlight relative overflow-hidden" ref="ctaRef">
      <!-- Background Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-0 left-0 w-96 h-96 bg-accent/10 rounded-full blur-3xl animate-float"></div>
        <div class="absolute bottom-0 right-0 w-72 h-72 bg-purple-500/10 rounded-full blur-3xl animate-float-delayed"></div>
      </div>
      
      <div class="max-w-5xl mx-auto text-center relative z-10">
        <div class="transform transition-all duration-700 ease-out"
             :class="ctaVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <h2 class="text-4xl md:text-5xl lg:text-6xl font-brand-bold text-text-primary mb-8 leading-tight">
            Ready to Transform Your
            <span class="text-accent bg-gradient-to-r from-accent to-purple-600 bg-clip-text text-transparent animate-text-shimmer bg-[length:200%_100%]">Station Operations?</span>
          </h2>
          <p class="text-xl md:text-2xl text-text-secondary mb-12 font-brand leading-relaxed transform transition-all duration-500 delay-200"
             :class="ctaVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'">
            Join thousands of organizations already using <span class="font-brand-semibold text-text-primary">Station List Pro</span> to optimize their operations.
          </p>
          <div class="flex flex-col sm:flex-row gap-6 justify-center transform transition-all duration-500 delay-400"
               :class="ctaVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'">
            <button class="group bg-accent hover:bg-purple-700 text-white font-brand-semibold px-12 py-6 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-300 transform hover:scale-105 hover:-translate-y-2 relative overflow-hidden">
              <!-- Button shine effect -->
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent -translate-x-full group-hover:translate-x-full transition-transform duration-700"></div>
              <span class="text-lg relative z-10">Start Your Free Trial</span>
            </button>
            <button class="group bg-white hover:bg-gray-50 text-accent border-2 border-accent/30 hover:border-accent font-brand-semibold px-12 py-6 rounded-2xl shadow-lg transition-all duration-300 transform hover:scale-105 hover:-translate-y-2 relative overflow-hidden">
              <!-- Button shine effect -->
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-accent/10 to-transparent -translate-x-full group-hover:translate-x-full transition-transform duration-700"></div>
              <span class="text-lg relative z-10">Schedule Demo</span>
            </button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted, reactive } from 'vue'

// Animation states
const heroVisible = ref(false)
const missionVisible = ref(false)
const teamVisible = ref(false)
const valuesVisible = ref(false)
const statsVisible = ref(false)
const ctaVisible = ref(false)

// Animated statistics
const animatedStats = reactive({
  activeStations: 0,
  teamExperts: 0,
  projectsDelivered: 0,
  yearsExcellence: 0
})

// Final target values
const targetStats = {
  activeStations: 15,
  teamExperts: 75,
  projectsDelivered: 500,
  yearsExcellence: 6
}

// Refs for intersection observers
const heroRef = ref(null)
const missionRef = ref(null)
const teamRef = ref(null)
const valuesRef = ref(null)
const statsRef = ref(null)
const ctaRef = ref(null)

// Intersection observers
let observers = []

// Counter animation function
const animateCounter = (current, target, setter, duration = 2000) => {
  const increment = target / (duration / 16) // 60fps
  const timer = setInterval(() => {
    if (current < target) {
      current += increment
      if (current >= target) {
        current = target
        clearInterval(timer)
      }
      setter(Math.floor(current))
    }
  }, 16)
  return timer
}

// Start all counter animations
const startCounterAnimations = () => {
  setTimeout(() => {
    animateCounter(0, targetStats.activeStations, (val) => animatedStats.activeStations = val, 1500)
  }, 200)
  
  setTimeout(() => {
    animateCounter(0, targetStats.teamExperts, (val) => animatedStats.teamExperts = val, 1800)
  }, 400)
  
  setTimeout(() => {
    animateCounter(0, targetStats.projectsDelivered, (val) => animatedStats.projectsDelivered = val, 2200)
  }, 600)
  
  setTimeout(() => {
    animateCounter(0, targetStats.yearsExcellence, (val) => animatedStats.yearsExcellence = val, 1200)
  }, 800)
}

const createObserver = (ref, visibilityRef, threshold = 0.2) => {
  return new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          visibilityRef.value = true
          
          // Start counter animations when stats section becomes visible
          if (ref === statsRef && !animatedStats.activeStations) {
            startCounterAnimations()
          }
        }
      })
    },
    {
      threshold,
      rootMargin: '0px 0px -50px 0px'
    }
  )
}

onMounted(() => {
  const sectionConfigs = [
    { ref: heroRef, visibility: heroVisible },
    { ref: missionRef, visibility: missionVisible },
    { ref: teamRef, visibility: teamVisible },
    { ref: valuesRef, visibility: valuesVisible },
    { ref: statsRef, visibility: statsVisible },
    { ref: ctaRef, visibility: ctaVisible }
  ]

  sectionConfigs.forEach(({ ref, visibility }) => {
    if (ref.value) {
      const observer = createObserver(ref, visibility)
      observer.observe(ref.value)
      observers.push(observer)
    }
  })
})

onUnmounted(() => {
  observers.forEach(observer => observer.disconnect())
})
</script>

<style scoped>
/* Hardware acceleration */
.transform {
  transform: translateZ(0);
  will-change: transform, opacity;
}

/* Professional transitions */
.transition-all {
  transition-property: all;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}

/* Custom animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

@keyframes float-delayed {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
}

@keyframes bounce-subtle {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-5px); }
}

@keyframes spin-slow {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

@keyframes text-shimmer {
  0% { background-position: -200% center; }
  100% { background-position: 200% center; }
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float-delayed 8s ease-in-out infinite;
  animation-delay: 2s;
}

.animate-bounce-subtle {
  animation: bounce-subtle 3s ease-in-out infinite;
}

.animate-spin-slow {
  animation: spin-slow 8s linear infinite;
}

.animate-text-shimmer {
  animation: text-shimmer 3s ease-in-out infinite;
}

.animate-shimmer {
  animation: shimmer 2s ease-in-out infinite;
}

/* Gradient utilities */
.bg-gradient-radial {
  background: radial-gradient(ellipse at center, var(--tw-gradient-stops));
}

/* Responsive text */
@media (max-width: 768px) {
  .text-8xl {
    font-size: 4rem;
  }
  
  .text-7xl {
    font-size: 3.5rem;
  }
  
  .text-6xl {
    font-size: 3rem;
  }
}

/* Enhanced shadow */
.shadow-3xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

/* Backdrop blur fallback */
.backdrop-blur-sm {
  backdrop-filter: blur(4px);
}

/* Custom scrollbar for webkit browsers */
::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #6366f1;
  border-radius: 3px;
}

::-webkit-scrollbar-thumb:hover {
  background: #4f46e5;
}
</style>
