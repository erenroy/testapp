<template>
  <div class="min-h-screen bg-white font-brand">
    
    <!-- Professional Hero Section -->
    <section class="relative py-20 lg:py-28 px-4 sm:px-6 lg:px-8 bg-gradient-to-br from-slate-50 via-gray-100 to-slate-200 overflow-hidden" ref="heroRef">
      <!-- Elegant Background Elements -->
      <div class="absolute inset-0">
        <div class="absolute inset-0 bg-[linear-gradient(rgba(148,163,184,0.1)_1px,transparent_1px),linear-gradient(90deg,rgba(148,163,184,0.1)_1px,transparent_1px)] bg-[size:60px_60px]"></div>
        <div class="absolute top-20 left-20 w-1.5 h-1.5 bg-slate-400 rounded-full animate-float"></div>
        <div class="absolute top-40 right-32 w-1 h-1 bg-slate-500 rounded-full animate-float-delayed"></div>
        <div class="absolute bottom-32 left-40 w-2 h-2 bg-slate-300 rounded-full animate-float" style="animation-delay: 2s;"></div>
        <div class="absolute top-32 right-20 w-1 h-1 bg-slate-600 rounded-full animate-float-delayed" style="animation-delay: 3s;"></div>
      </div>
      
      <div class="max-w-7xl mx-auto relative z-10">
        <div class="text-center">
          <!-- Professional Badge -->
          <div class="inline-flex items-center gap-3 bg-white/80 backdrop-blur-lg rounded-full px-8 py-4 mb-12 border border-slate-200 shadow-lg transform transition-all duration-700 ease-out"
               :class="heroVisible ? 'opacity-100 translate-y-0 scale-100' : 'opacity-0 translate-y-8 scale-95'">
            <div class="w-2 h-2 bg-slate-500 rounded-full animate-pulse"></div>
            <span class="text-slate-700 font-brand-medium text-sm tracking-wide">Platform Overview</span>
            <div class="w-2 h-2 bg-slate-500 rounded-full animate-pulse"></div>
          </div>
          
          <!-- Updated Main Headline (REMOVED UNDERLINE) -->
          <div class="relative mb-8 transform transition-all duration-700 ease-out delay-200"
               :class="heroVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
            <h1 class="text-5xl md:text-6xl lg:text-7xl font-brand-bold text-slate-800 leading-tight">
              Next-Generation
              <div class="relative inline-block mt-2">
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-accent via-purple-600 to-cyan-500 animate-text-shimmer bg-[length:200%_100%]">
                  Station Intelligence
                </span>
                <!-- REMOVED: The underline div -->
              </div>
              Platform
            </h1>
          </div>
          
          <!-- Professional Description -->
          <p class="max-w-4xl mx-auto text-xl md:text-2xl text-slate-600 leading-relaxed mb-12 font-brand transform transition-all duration-700 ease-out delay-400"
             :class="heroVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
            Experience the future of station management with <span class="text-slate-800 font-brand-semibold">AI-powered automation</span>, 
            <span class="text-slate-700 font-brand-semibold">real-time intelligence</span>, and 
            <span class="text-slate-700 font-brand-semibold">predictive analytics</span> all in one unified ecosystem.
          </p>
          
          <!-- Updated CTA Buttons with ACCENT COLOR -->
          <div class="flex flex-col sm:flex-row gap-4 justify-center transform transition-all duration-700 ease-out delay-600"
               :class="heroVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
            <button class="group relative bg-accent hover:bg-purple-700 text-white font-brand-semibold px-12 py-4 rounded-xl shadow-xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
              <span class="relative z-10 flex items-center gap-3">
                <span>Explore Platform</span>
                <svg class="w-5 h-5 transition-transform duration-200 group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </span>
            </button>
            <button class="group relative bg-white hover:bg-slate-50 text-accent border-2 border-accent/30 hover:border-accent font-brand-semibold px-12 py-4 rounded-xl shadow-lg transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-slate-100/50 to-transparent -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
              <span class="relative z-10 flex items-center gap-3">
                <span>Watch Demo</span>
                <svg class="w-5 h-5 transition-transform duration-200 group-hover:scale-110" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h1m4 0h1m-6 4h.01M19 10a9 9 0 11-18 0 9 9 0 0118 0z"/>
                </svg>
              </span>
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Professional Dashboard Preview -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-white" ref="dashboardRef">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16 transform transition-all duration-700 ease-out"
             :class="dashboardVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <h2 class="text-4xl md:text-5xl font-brand-bold text-slate-800 mb-4">
            See the Platform in <span class="text-accent">Action</span>
          </h2>
          <p class="text-xl text-slate-600 max-w-3xl mx-auto">
            Get a glimpse of our intuitive interface designed for maximum efficiency and user experience.
          </p>
        </div>
        
        <!-- Professional Dashboard Mock -->
        <div class="relative max-w-6xl mx-auto transform transition-all duration-700 ease-out delay-200"
             :class="dashboardVisible ? 'opacity-100 translate-y-0 scale-100' : 'opacity-0 translate-y-8 scale-95'">
          <div class="bg-white rounded-2xl shadow-2xl border border-slate-200 overflow-hidden hover:shadow-3xl transition-all duration-500">
            <!-- Dashboard Header -->
            <div class="bg-gradient-to-r from-slate-800 to-slate-700 p-6">
              <div class="flex items-center justify-between">
                <div class="flex items-center gap-4">
                  <div class="w-12 h-12 bg-slate-600 rounded-xl flex items-center justify-center shadow-lg">
                    <span class="text-white font-brand-bold text-lg">S</span>
                  </div>
                  <div>
                    <h3 class="text-white font-brand-bold text-lg">Station Control Center</h3>
                    <p class="text-slate-300 text-sm">Real-time Operations Dashboard</p>
                  </div>
                </div>
                <div class="flex items-center gap-2">
                  <div class="w-2 h-2 bg-emerald-400 rounded-full animate-pulse"></div>
                  <span class="text-emerald-400 text-sm font-brand-medium">Live</span>
                </div>
              </div>
            </div>
            
            <!-- Dashboard Content -->
            <div class="p-8">
              <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- Main Analytics -->
                <div class="lg:col-span-2">
                  <div class="bg-slate-50 rounded-xl p-6 border border-slate-200">
                    <h4 class="text-lg font-brand-bold text-slate-800 mb-4">Station Performance Analytics</h4>
                    <!-- UPDATED CHART with actual line graph -->
                    <div class="relative h-64 bg-white rounded-lg p-6 shadow-sm border border-slate-100">
                      <svg class="w-full h-full" viewBox="0 0 400 200" preserveAspectRatio="xMidYMid meet">
                        <!-- Grid lines -->
                        <defs>
                          <pattern id="grid" width="40" height="20" patternUnits="userSpaceOnUse">
                            <path d="M 40 0 L 0 0 0 20" fill="none" stroke="#e2e8f0" stroke-width="1"/>
                          </pattern>
                        </defs>
                        <rect width="100%" height="100%" fill="url(#grid)" />
                        
                        <!-- Animated line chart -->
                        <polyline 
                          fill="none" 
                          stroke="#5138ee" 
                          stroke-width="3" 
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          points="40,120 80,80 120,100 160,60 200,80 240,40 280,72 320,48 360,32"
                          class="animate-pulse"
                        />
                        
                        <!-- Data points -->
                        <circle cx="40" cy="120" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="80" cy="80" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="120" cy="100" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="160" cy="60" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="200" cy="80" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="240" cy="40" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="280" cy="72" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="320" cy="48" r="4" fill="#5138ee" class="animate-pulse"/>
                        <circle cx="360" cy="32" r="4" fill="#5138ee" class="animate-pulse"/>
                      </svg>
                      
                      <!-- Day labels -->
                      <div class="flex items-end justify-between absolute bottom-2 left-6 right-6">
                        <span class="text-xs text-slate-500 font-brand-medium">Mon</span>
                        <span class="text-xs text-slate-500 font-brand-medium">Tue</span>
                        <span class="text-xs text-slate-500 font-brand-medium">Wed</span>
                        <span class="text-xs text-slate-500 font-brand-medium">Thu</span>
                        <span class="text-xs text-slate-500 font-brand-medium">Fri</span>
                        <span class="text-xs text-slate-500 font-brand-medium">Sat</span>
                        <span class="text-xs text-slate-500 font-brand-medium">Sun</span>
                      </div>
                    </div>
                  </div>
                </div>
                
                <!-- Professional Stats -->
                <div class="space-y-6">
                  <!-- Active Stations -->
                  <div class="bg-white rounded-xl p-6 shadow-sm border border-slate-200 hover:shadow-md transition-all duration-300">
                    <div class="flex items-center justify-between mb-3">
                      <h4 class="text-sm font-brand-medium text-slate-700">Active Stations</h4>
                      <div class="w-2 h-2 bg-emerald-500 rounded-full animate-pulse"></div>
                    </div>
                    <div class="text-3xl font-brand-bold text-slate-800">{{ animatedStats.activeStations }}K</div>
                    <p class="text-sm text-slate-500 mt-1">+12% from last month</p>
                  </div>
                  
                  <!-- System Health -->
                  <div class="bg-white rounded-xl p-6 shadow-sm border border-slate-200 hover:shadow-md transition-all duration-300">
                    <div class="flex items-center justify-between mb-3">
                      <h4 class="text-sm font-brand-medium text-slate-700">System Health</h4>
                      <div class="w-2 h-2 bg-emerald-500 rounded-full animate-pulse"></div>
                    </div>
                    <div class="text-3xl font-brand-bold text-slate-800">{{ animatedStats.uptime }}%</div>
                    <p class="text-sm text-slate-500 mt-1">Operational status</p>
                  </div>
                  
                  <!-- Response Time -->
                  <div class="bg-white rounded-xl p-6 shadow-sm border border-slate-200 hover:shadow-md transition-all duration-300">
                    <div class="flex items-center justify-between mb-3">
                      <h4 class="text-sm font-brand-medium text-slate-700">Avg Response</h4>
                      <div class="w-2 h-2 bg-emerald-500 rounded-full animate-pulse"></div>
                    </div>
                    <div class="text-3xl font-brand-bold text-slate-800">{{ animatedStats.responseTime }}ms</div>
                    <p class="text-sm text-slate-500 mt-1">System performance</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Professional Capabilities Grid -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-slate-50" ref="capabilitiesRef">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-20 transform transition-all duration-700 ease-out"
             :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <h2 class="text-4xl md:text-5xl font-brand-bold text-slate-800 mb-6">
            Platform <span class="text-accent">Capabilities</span>
          </h2>
          <p class="max-w-3xl mx-auto text-xl text-slate-600 leading-relaxed">
            Comprehensive tools designed to optimize every aspect of your station management operations.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- AI-Powered Analytics -->
          <div class="group relative bg-white rounded-2xl p-8 border border-slate-200 hover:border-slate-300 transition-all duration-500 transform hover:-translate-y-2 hover:shadow-xl overflow-hidden"
               :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: capabilitiesVisible ? '100ms' : '0ms' }">
            <div class="absolute top-0 right-0 w-32 h-32 bg-slate-100/50 rounded-full blur-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-16 h-16 bg-slate-800 rounded-2xl mb-6 flex items-center justify-center shadow-lg group-hover:scale-110 transition-transform duration-300">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-brand-bold text-slate-800 mb-4">AI-Powered Analytics</h3>
              <p class="text-slate-600 leading-relaxed mb-6">
                Advanced machine learning algorithms analyze patterns, predict issues, and optimize operations automatically.
              </p>
              <div class="flex items-center text-accent font-brand-medium text-sm group-hover:text-slate-800 transition-colors">
                <span>Learn more</span>
                <svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </div>
            </div>
          </div>

          <!-- Real-time Monitoring -->
          <div class="group relative bg-white rounded-2xl p-8 border border-slate-200 hover:border-slate-300 transition-all duration-500 transform hover:-translate-y-2 hover:shadow-xl overflow-hidden"
               :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: capabilitiesVisible ? '200ms' : '0ms' }">
            <div class="absolute top-0 right-0 w-32 h-32 bg-slate-100/50 rounded-full blur-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-16 h-16 bg-slate-700 rounded-2xl mb-6 flex items-center justify-center shadow-lg group-hover:scale-110 transition-transform duration-300">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-brand-bold text-slate-800 mb-4">Real-time Monitoring</h3>
              <p class="text-slate-600 leading-relaxed mb-6">
                Monitor all station activities with live dashboards, instant alerts, and comprehensive status tracking.
              </p>
              <div class="flex items-center text-accent font-brand-medium text-sm group-hover:text-slate-800 transition-colors">
                <span>Learn more</span>
                <svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </div>
            </div>
          </div>

          <!-- Smart Automation -->
          <div class="group relative bg-white rounded-2xl p-8 border border-slate-200 hover:border-slate-300 transition-all duration-500 transform hover:-translate-y-2 hover:shadow-xl overflow-hidden"
               :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: capabilitiesVisible ? '300ms' : '0ms' }">
            <div class="absolute top-0 right-0 w-32 h-32 bg-slate-100/50 rounded-full blur-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-16 h-16 bg-slate-600 rounded-2xl mb-6 flex items-center justify-center shadow-lg group-hover:scale-110 transition-transform duration-300">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-brand-bold text-slate-800 mb-4">Smart Automation</h3>
              <p class="text-slate-600 leading-relaxed mb-6">
                Intelligent workflows that automate routine tasks, reduce errors, and increase operational efficiency.
              </p>
              <div class="flex items-center text-accent font-brand-medium text-sm group-hover:text-slate-800 transition-colors">
                <span>Learn more</span>
                <svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </div>
            </div>
          </div>

          <!-- Security & Compliance -->
          <div class="group relative bg-white rounded-2xl p-8 border border-slate-200 hover:border-slate-300 transition-all duration-500 transform hover:-translate-y-2 hover:shadow-xl overflow-hidden"
               :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: capabilitiesVisible ? '400ms' : '0ms' }">
            <div class="absolute top-0 right-0 w-32 h-32 bg-slate-100/50 rounded-full blur-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-16 h-16 bg-slate-500 rounded-2xl mb-6 flex items-center justify-center shadow-lg group-hover:scale-110 transition-transform duration-300">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-brand-bold text-slate-800 mb-4">Security & Compliance</h3>
              <p class="text-slate-600 leading-relaxed mb-6">
                Enterprise-grade security with advanced encryption, access controls, and compliance frameworks.
              </p>
              <div class="flex items-center text-accent font-brand-medium text-sm group-hover:text-slate-800 transition-colors">
                <span>Learn more</span>
                <svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </div>
            </div>
          </div>

          <!-- Cloud Integration -->
          <div class="group relative bg-white rounded-2xl p-8 border border-slate-200 hover:border-slate-300 transition-all duration-500 transform hover:-translate-y-2 hover:shadow-xl overflow-hidden"
               :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: capabilitiesVisible ? '500ms' : '0ms' }">
            <div class="absolute top-0 right-0 w-32 h-32 bg-slate-100/50 rounded-full blur-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-16 h-16 bg-slate-700 rounded-2xl mb-6 flex items-center justify-center shadow-lg group-hover:scale-110 transition-transform duration-300">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-brand-bold text-slate-800 mb-4">Cloud Integration</h3>
              <p class="text-slate-600 leading-relaxed mb-6">
                Seamless cloud connectivity with scalable infrastructure and multi-platform synchronization.
              </p>
              <div class="flex items-center text-accent font-brand-medium text-sm group-hover:text-slate-800 transition-colors">
                <span>Learn more</span>
                <svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </div>
            </div>
          </div>

          <!-- Mobile Experience -->
          <div class="group relative bg-white rounded-2xl p-8 border border-slate-200 hover:border-slate-300 transition-all duration-500 transform hover:-translate-y-2 hover:shadow-xl overflow-hidden"
               :class="capabilitiesVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'"
               :style="{ transitionDelay: capabilitiesVisible ? '600ms' : '0ms' }">
            <div class="absolute top-0 right-0 w-32 h-32 bg-slate-100/50 rounded-full blur-3xl"></div>
            
            <div class="relative z-10">
              <div class="w-16 h-16 bg-slate-600 rounded-2xl mb-6 flex items-center justify-center shadow-lg group-hover:scale-110 transition-transform duration-300">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-brand-bold text-slate-800 mb-4">Mobile Experience</h3>
              <p class="text-slate-600 leading-relaxed mb-6">
                Native mobile apps with offline capabilities for managing operations anywhere, anytime.
              </p>
              <div class="flex items-center text-accent font-brand-medium text-sm group-hover:text-slate-800 transition-colors">
                <span>Learn more</span>
                <svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Professional Performance Stats -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-slate-800" ref="statsRef">
      <div class="max-w-7xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-brand-bold text-white mb-4">
            Platform Performance <span class="text-slate-300">Metrics</span>
          </h2>
          <p class="text-xl text-slate-400">Real-time performance indicators that showcase our platform's capabilities</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8 text-center">
          <!-- Daily Operations -->
          <div class="group bg-slate-700/50 backdrop-blur-sm rounded-2xl p-8 border border-slate-600 hover:border-slate-500 transition-all duration-500 transform hover:scale-105"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '100ms' : '0ms' }">
            <div class="w-12 h-12 bg-slate-600 rounded-xl mx-auto mb-6 flex items-center justify-center group-hover:bg-slate-500 transition-colors duration-300">
              <svg class="w-6 h-6 text-slate-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
              </svg>
            </div>
            <div class="text-4xl font-brand-bold text-white mb-2">{{ animatedStats.processingSpeed }}M+</div>
            <p class="text-slate-400 font-brand-medium">Daily Operations</p>
          </div>
          
          <!-- Active Stations -->
          <div class="group bg-slate-700/50 backdrop-blur-sm rounded-2xl p-8 border border-slate-600 hover:border-slate-500 transition-all duration-500 transform hover:scale-105"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '200ms' : '0ms' }">
            <div class="w-12 h-12 bg-slate-600 rounded-xl mx-auto mb-6 flex items-center justify-center group-hover:bg-slate-500 transition-colors duration-300">
              <svg class="w-6 h-6 text-slate-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
              </svg>
            </div>
            <div class="text-4xl font-brand-bold text-white mb-2">{{ animatedStats.activeStations }}K</div>
            <p class="text-slate-400 font-brand-medium">Active Stations</p>
          </div>
          
          <!-- Response Time -->
          <div class="group bg-slate-700/50 backdrop-blur-sm rounded-2xl p-8 border border-slate-600 hover:border-slate-500 transition-all duration-500 transform hover:scale-105"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '300ms' : '0ms' }">
            <div class="w-12 h-12 bg-slate-600 rounded-xl mx-auto mb-6 flex items-center justify-center group-hover:bg-slate-500 transition-colors duration-300">
              <svg class="w-6 h-6 text-slate-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
            <div class="text-4xl font-brand-bold text-white mb-2">{{ animatedStats.responseTime }}ms</div>
            <p class="text-slate-400 font-brand-medium">Response Time</p>
          </div>
          
          <!-- System Uptime -->
          <div class="group bg-slate-700/50 backdrop-blur-sm rounded-2xl p-8 border border-slate-600 hover:border-slate-500 transition-all duration-500 transform hover:scale-105"
               :class="statsVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'"
               :style="{ transitionDelay: statsVisible ? '400ms' : '0ms' }">
            <div class="w-12 h-12 bg-slate-600 rounded-xl mx-auto mb-6 flex items-center justify-center group-hover:bg-slate-500 transition-colors duration-300">
              <svg class="w-6 h-6 text-slate-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
              </svg>
            </div>
            <div class="text-4xl font-brand-bold text-white mb-2">{{ animatedStats.uptime }}%</div>
            <p class="text-slate-400 font-brand-medium">System Uptime</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Professional CTA -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-white" ref="ctaRef">
      <div class="max-w-5xl mx-auto text-center">
        <div class="transform transition-all duration-700 ease-out"
             :class="ctaVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'">
          <h2 class="text-4xl md:text-5xl font-brand-bold text-slate-800 mb-8 leading-tight">
            Experience the Future of
            <span class="text-accent">Station Management</span>
          </h2>
          <p class="text-xl text-slate-600 mb-12 leading-relaxed transform transition-all duration-500 delay-200"
             :class="ctaVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'">
            Join industry leaders who trust <span class="font-brand-semibold text-slate-800">Station List Pro</span> to power their critical operations with next-generation technology.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center transform transition-all duration-500 delay-400"
               :class="ctaVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'">
            <button class="group relative bg-accent hover:bg-purple-700 text-white font-brand-semibold px-12 py-4 rounded-xl shadow-xl transition-all duration-500 transform hover:scale-105 hover:-translate-y-1 overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
              <span class="relative z-10">Start Free Trial</span>
            </button>
            <button class="group bg-white hover:bg-slate-50 text-accent border-2 border-accent/30 hover:border-accent font-brand-semibold px-12 py-4 rounded-xl shadow-lg transition-all duration-300 transform hover:scale-105 hover:-translate-y-1 relative overflow-hidden">
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-slate-100/50 to-transparent -skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-1000"></div>
              <span class="relative z-10">Schedule Demo</span>
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
const dashboardVisible = ref(false)
const capabilitiesVisible = ref(false)
const statsVisible = ref(false)
const ctaVisible = ref(false)

// Animated statistics
const animatedStats = reactive({
  processingSpeed: 0,
  activeStations: 0,
  responseTime: 0,
  uptime: 0
})

// Final target values
const targetStats = {
  processingSpeed: 2,
  activeStations: 15,
  responseTime: 150,
  uptime: 99.9
}

// Refs for intersection observers
const heroRef = ref(null)
const dashboardRef = ref(null)
const capabilitiesRef = ref(null)
const statsRef = ref(null)
const ctaRef = ref(null)

// Intersection observers
let observers = []

// Counter animation function
const animateCounter = (current, target, setter, duration = 2000, isDecimal = false) => {
  const increment = target / (duration / 16) // 60fps
  const timer = setInterval(() => {
    if (current < target) {
      current += increment
      if (current >= target) {
        current = target
        clearInterval(timer)
      }
      setter(isDecimal ? parseFloat(current.toFixed(1)) : Math.floor(current))
    }
  }, 16)
  return timer
}

// Start all counter animations
const startCounterAnimations = () => {
  setTimeout(() => {
    animateCounter(0, targetStats.processingSpeed, (val) => animatedStats.processingSpeed = val, 1500)
  }, 200)
  
  setTimeout(() => {
    animateCounter(0, targetStats.activeStations, (val) => animatedStats.activeStations = val, 1800)
  }, 400)
  
  setTimeout(() => {
    animateCounter(0, targetStats.responseTime, (val) => animatedStats.responseTime = val, 2200)
  }, 600)
  
  setTimeout(() => {
    animateCounter(0, targetStats.uptime, (val) => animatedStats.uptime = val, 1200, true)
  }, 800)
}

const createObserver = (ref, visibilityRef, threshold = 0.2) => {
  return new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          visibilityRef.value = true
          
          // Start counter animations when stats section becomes visible
          if (ref === statsRef && !animatedStats.processingSpeed) {
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
    { ref: dashboardRef, visibility: dashboardVisible },
    { ref: capabilitiesRef, visibility: capabilitiesVisible },
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

/* Beautiful floating animations */
@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(180deg); }
}

@keyframes float-delayed {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-15px) rotate(-180deg); }
}

@keyframes text-shimmer {
  0% { background-position: -200% center; }
  100% { background-position: 200% center; }
}

.animate-float {
  animation: float 8s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float-delayed 10s ease-in-out infinite;
  animation-delay: 2s;
}

.animate-text-shimmer {
  animation: text-shimmer 3s ease-in-out infinite;
}

/* Professional shadow */
.shadow-3xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
}

/* Responsive text */
@media (max-width: 768px) {
  .text-7xl {
    font-size: 3.5rem;
  }
  
  .text-6xl {
    font-size: 3rem;
  }
  
  .text-5xl {
    font-size: 2.5rem;
  }
}
</style>
