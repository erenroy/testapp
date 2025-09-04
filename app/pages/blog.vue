<template>
  <div class="min-h-screen bg-gradient-to-br from-primary to-accentlight font-brand relative overflow-hidden">
    <!-- Simple Line Grid Background -->
    <div class="absolute inset-0 opacity-20">
      <div 
        class="w-full h-full" 
        style="
          background-image: 
            linear-gradient(rgba(136, 136, 136, 0.3) 1px, transparent 1px),
            linear-gradient(90deg, rgba(136, 136, 136, 0.3) 1px, transparent 1px);
          background-size: 40px 40px;
        "
      ></div>
    </div>
    
    <!-- Hero Section -->
    <section class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-8 pb-6 relative z-10">
      <div class="text-center">
        <!-- Blog Overview Badge -->
        <div class="inline-flex items-center px-6 py-3 bg-white/90 backdrop-blur-sm rounded-full shadow-lg border border-border/20 mb-6">
          <span class="w-2 h-2 bg-accent rounded-full mr-3"></span>
          <span class="text-text-primary font-brand-medium text-sm">Tech Blog & Insights</span>
          <span class="w-2 h-2 bg-accent rounded-full ml-3"></span>
        </div>
        
        <!-- Blog Main Heading -->
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-brand-bold text-text-primary mb-4 leading-tight">
          Latest 
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 via-purple-500 to-purple-600">
            Tech Articles & Stories
          </span>
        </h1>
        
        <p class="text-lg md:text-xl text-text-secondary max-w-3xl mx-auto leading-relaxed">
          Stay ahead of the curve with expert insights on web development, design trends, 
          and the latest technology innovations shaping our digital future.
        </p>
      </div>
    </section>

    <!-- Search Bar Section -->
    <section class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pb-6 relative z-10">
      <div class="max-w-2xl mx-auto">
        <div class="relative">
          <div class="absolute inset-y-0 left-0 pl-4 flex items-center pointer-events-none">
            <svg class="h-5 w-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
          </div>
          <input
            v-model="searchQuery"
            type="text"
            placeholder="Search articles by title..."
            class="w-full pl-12 pr-4 py-4 bg-white/90 backdrop-blur-lg border-2 border-accent/30 rounded-2xl shadow-xl focus:ring-2 focus:ring-accent focus:border-accent transition-all duration-300 text-text-primary placeholder-gray-400 text-lg"
          />
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6 relative z-10">
      <!-- Blog Grid -->
      <div class="grid gap-8 lg:grid-cols-3 md:grid-cols-2 grid-cols-1">
        <!-- Blog Card 1 -->
        <article v-show="isVisible('Advanced React Patterns for Enterprise Applications')" class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
              alt="Web Development"
              class="w-full h-56 object-cover group-hover:scale-110 transition-transform duration-700"
            />
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 text-xs font-brand-medium bg-accent text-white rounded-full shadow-lg">
                Technology
              </span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-center gap-2 mb-4 text-text-muted text-sm">
              <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
              </svg>
              <span>5 min read</span>
              <span>•</span>
              <span>March 15, 2025</span>
            </div>
            
            <h3 class="text-xl font-brand-semibold text-text-primary mb-3 line-clamp-2 group-hover:text-accent transition-colors">
              Advanced React Patterns for Enterprise Applications
            </h3>
            
            <p class="text-text-secondary mb-6 line-clamp-3 leading-relaxed">
              Learn about compound components, render props, and custom hooks that will take your React development to the next level.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-3">
                <img 
                  src="https://images.unsplash.com/photo-1494790108755-2616b612b169?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Sarah Johnson</p>
                  <p class="text-xs text-text-muted">Senior Developer</p>
                </div>
              </div>
             <NuxtLink 
                  to="/blog1" 
                  class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                  Read More
              </NuxtLink>

            </div>
          </div>
        </article>

        <!-- Blog Card 2 -->
        <article v-show="isVisible('Creating Delightful Micro-Interactions with CSS')" class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1558655146-d09347e92766?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2064&q=80" 
              alt="UI/UX Design"
              class="w-full h-56 object-cover group-hover:scale-110 transition-transform duration-700"
            />
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 text-xs font-brand-medium bg-accent text-white rounded-full shadow-lg">
                Design
              </span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-center gap-2 mb-4 text-text-muted text-sm">
              <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
              </svg>
              <span>7 min read</span>
              <span>•</span>
              <span>March 12, 2025</span>
            </div>
            
            <h3 class="text-xl font-brand-semibold text-text-primary mb-3 line-clamp-2 group-hover:text-accent transition-colors">
              Creating Delightful Micro-Interactions with CSS
            </h3>
            
            <p class="text-text-secondary mb-6 line-clamp-3 leading-relaxed">
              Discover how subtle animations and transitions can dramatically improve user experience and engagement.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-3">
                <img 
                  src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Mike Chen</p>
                  <p class="text-xs text-text-muted">UI/UX Designer</p>
                </div>
              </div>
              <NuxtLink 
                  to="/blog1" 
                  class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                  Read More
              </NuxtLink>
            </div>
          </div>
        </article>

        <!-- Blog Card 3 -->
        <article v-show="isVisible('Data-Driven Product Decisions: A Complete Framework')" class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2015&q=80" 
              alt="Business Analytics"
              class="w-full h-56 object-cover group-hover:scale-110 transition-transform duration-700"
            />
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 text-xs font-brand-medium bg-accent text-white rounded-full shadow-lg">
                Business
              </span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-center gap-2 mb-4 text-text-muted text-sm">
              <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
              </svg>
              <span>6 min read</span>
              <span>•</span>
              <span>March 10, 2025</span>
            </div>
            
            <h3 class="text-xl font-brand-semibold text-text-primary mb-3 line-clamp-2 group-hover:text-accent transition-colors">
              Data-Driven Product Decisions: A Complete Framework
            </h3>
            
            <p class="text-text-secondary mb-6 line-clamp-3 leading-relaxed">
              Learn how to leverage analytics and user feedback to make informed product decisions that drive growth.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-3">
                <img 
                  src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Emma Davis</p>
                  <p class="text-xs text-text-muted">Product Manager</p>
                </div>
              </div>
              <NuxtLink 
                  to="/blog1" 
                  class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                  Read More
              </NuxtLink>
            </div>
          </div>
        </article>

        <!-- Blog Card 4 -->
        <article v-show="isVisible('Vue 3 Composition API: Best Practices and Patterns')" class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1517180102446-f3ece451e9d8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
              alt="Vue.js Development"
              class="w-full h-56 object-cover group-hover:scale-110 transition-transform duration-700"
            />
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 text-xs font-brand-medium bg-accent text-white rounded-full shadow-lg">
                Development
              </span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-center gap-2 mb-4 text-text-muted text-sm">
              <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
              </svg>
              <span>8 min read</span>
              <span>•</span>
              <span>March 8, 2025</span>
            </div>
            
            <h3 class="text-xl font-brand-semibold text-text-primary mb-3 line-clamp-2 group-hover:text-accent transition-colors">
              Vue 3 Composition API: Best Practices and Patterns
            </h3>
            
            <p class="text-text-secondary mb-6 line-clamp-3 leading-relaxed">
              Master the Composition API with real-world examples and learn how to structure scalable Vue applications.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-3">
                <img 
                  src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Alex Rodriguez</p>
                  <p class="text-xs text-text-muted">Vue.js Expert</p>
                </div>
              </div>
             <NuxtLink 
                  to="/blog1" 
                  class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                  Read More
              </NuxtLink>
            </div>
          </div>
        </article>

        <!-- Blog Card 5 -->
        <article v-show="isVisible('Tailwind CSS: Advanced Techniques for Production Apps')" class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2155&q=80" 
              alt="CSS Framework"
              class="w-full h-56 object-cover group-hover:scale-110 transition-transform duration-700"
            />
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 text-xs font-brand-medium bg-accent text-white rounded-full shadow-lg">
                Tutorial
              </span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-center gap-2 mb-4 text-text-muted text-sm">
              <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
              </svg>
              <span>10 min read</span>
              <span>•</span>
              <span>March 5, 2025</span>
            </div>
            
            <h3 class="text-xl font-brand-semibold text-text-primary mb-3 line-clamp-2 group-hover:text-accent transition-colors">
              Tailwind CSS: Advanced Techniques for Production Apps
            </h3>
            
            <p class="text-text-secondary mb-6 line-clamp-3 leading-relaxed">
              Optimize your Tailwind workflow with custom utilities, component extraction, and performance optimization techniques.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-3">
                <img 
                  src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=688&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Lisa Thompson</p>
                  <p class="text-xs text-text-muted">CSS Specialist</p>
                </div>
              </div>
              <NuxtLink 
                  to="/blog1" 
                  class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                  Read More
              </NuxtLink>
            </div>
          </div>
        </article>

        <!-- Blog Card 6 -->
        <article v-show="isVisible('Building Resilient Teams in the Digital Age')" class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
              alt="Digital Transformation"
              class="w-full h-56 object-cover group-hover:scale-110 transition-transform duration-700"
            />
            <div class="absolute top-4 left-4">
              <span class="px-3 py-1 text-xs font-brand-medium bg-accent text-white rounded-full shadow-lg">
                Strategy
              </span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-center gap-2 mb-4 text-text-muted text-sm">
              <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
              </svg>
              <span>12 min read</span>
              <span>•</span>
              <span>March 3, 2025</span>
            </div>
            
            <h3 class="text-xl font-brand-semibold text-text-primary mb-3 line-clamp-2 group-hover:text-accent transition-colors">
              Building Resilient Teams in the Digital Age
            </h3>
            
            <p class="text-text-secondary mb-6 line-clamp-3 leading-relaxed">
              Strategies for creating high-performing remote teams and fostering collaboration in distributed environments.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-3">
                <img 
                  src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">David Kim</p>
                  <p class="text-xs text-text-muted">Team Lead</p>
                </div>
              </div>
              <NuxtLink 
                  to="/blog1" 
                  class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                  Read More
              </NuxtLink>
            </div>
          </div>
        </article>
      </div>

      <!-- Load More Section -->
      <div class="mt-16 text-center">
        <button class="px-10 py-4 bg-gradient-to-r from-accent to-purple-600 text-white font-brand-semibold rounded-xl hover:shadow-xl transition-all duration-300 transform hover:scale-105">
          Load More Articles
        </button>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const searchQuery = ref('')

const isVisible = (title) => {
  if (!searchQuery.value) return true
  return title.toLowerCase().includes(searchQuery.value.toLowerCase())
}
</script>

<style scoped>
.line-clamp-2 {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.line-clamp-3 {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

/* Custom scrollbar for better aesthetics */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #f1f5f9;
}

::-webkit-scrollbar-thumb {
  background: #5138ee;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #4c34d4;
}
</style>
