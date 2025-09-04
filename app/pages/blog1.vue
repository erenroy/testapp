<template>
  <div class="min-h-screen bg-gradient-to-br from-primary to-accentlight font-brand relative overflow-hidden mt-6">

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
    
    <!-- Article Content -->
   <article class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 pt-[1vh] pb-8 relative z-10">

      <!-- Article Header -->
      <header class="mb-8 animate-fade-in-up">
        <h1 class="text-3xl md:text-4xl lg:text-5xl font-brand-bold text-text-primary mb-6 leading-tight">
          Advanced Coding Patterns for Enterprise Applications
        </h1>
        
        <!-- Article Meta -->
        <div class="flex flex-wrap items-center gap-6 mb-6 text-text-muted">
          <div class="flex items-center gap-2">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z" clip-rule="evenodd" />
            </svg>
            <span>5 min read</span>
          </div>
          <div class="flex items-center gap-2">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd" />
            </svg>
            <span>March 15, 2025</span>
          </div>
          <div class="flex items-center gap-2">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd" />
            </svg>
            <span>Sarah Johnson</span>
          </div>
        </div>
        
        <!-- Author Info -->
        <div class="bg-white/80 backdrop-blur-lg rounded-2xl p-6 border border-white/20 shadow-xl">
          <div class="flex items-center gap-4">
            <img 
              src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
              alt="Sarah Johnson"
              class="w-16 h-16 rounded-full object-cover ring-2 ring-accent/20"
            />
            <div>
              <h3 class="font-brand-semibold text-text-primary text-lg">Sarah Johnson</h3>
              <p class="text-text-muted mb-2">Senior Developer at TechCorp</p>
              <p class="text-text-secondary text-sm leading-relaxed">
                Passionate about React development with 8+ years of experience building scalable enterprise applications.
              </p>
            </div>
          </div>
        </div>
      </header>

      <!-- Hero Image Section -->
      <section class="mb-8 animate-fade-in-delayed">
        <div class="h-64 md:h-80 relative overflow-hidden rounded-2xl shadow-xl">
          <img 
            src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" 
            alt="Developer working on laptop"
            class="w-full h-full object-cover"
          />
          <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent"></div>
        </div>
      </section>

      <!-- Article Content -->
      <div class="max-w-4xl mx-auto">
        <!-- Introduction -->
        <div class="bg-white/80 backdrop-blur-lg rounded-2xl p-8 border border-white/20 shadow-xl mb-8 animate-fade-in-scroll">
          <p class="text-xl text-text-secondary leading-relaxed mb-6">
            React has evolved significantly over the years, and with it, the patterns and practices for building robust enterprise applications. In this comprehensive guide, we'll explore advanced React patterns that can help you create more maintainable, scalable, and performant applications.
          </p>
          
          <p class="text-lg text-text-secondary leading-relaxed">
            Whether you're working on a large-scale enterprise project or looking to level up your React skills, these patterns will provide you with the tools and knowledge needed to architect better applications.
          </p>
        </div>

        <!-- Main Content Sections -->
        <div class="space-y-8">
          <section class="bg-white/80 backdrop-blur-lg rounded-2xl p-8 border border-white/20 shadow-xl animate-fade-in-scroll">
            <h2 class="text-3xl font-brand-semibold text-text-primary mb-6">1. Compound Components Pattern</h2>
            <p class="text-lg text-text-secondary leading-relaxed mb-6">
              The Compound Components pattern is a powerful way to create flexible and reusable components. It allows you to create components that work together to form a complete UI element, while giving users the flexibility to compose them as needed.
            </p>
            <div class="bg-gray-900 rounded-lg p-6 my-6 overflow-x-auto">
              <pre class="text-green-400 text-sm leading-relaxed">
<code>&lt;Tabs&gt;
  &lt;TabList&gt;
    &lt;Tab&gt;Tab 1&lt;/Tab&gt;
    &lt;Tab&gt;Tab 2&lt;/Tab&gt;
  &lt;/TabList&gt;
  &lt;TabPanels&gt;
    &lt;TabPanel&gt;Content 1&lt;/TabPanel&gt;
    &lt;TabPanel&gt;Content 2&lt;/TabPanel&gt;
  &lt;/TabPanels&gt;
&lt;/Tabs&gt;</code>
              </pre>
            </div>
            <p class="text-lg text-text-secondary leading-relaxed">
              This pattern provides implicit state sharing between components and creates a more intuitive API for developers using your components. It's particularly useful when you want to give users maximum flexibility in how they compose your components.
            </p>
          </section>

          <section class="bg-white/80 backdrop-blur-lg rounded-2xl p-8 border border-white/20 shadow-xl animate-fade-in-scroll">
            <h2 class="text-3xl font-brand-semibold text-text-primary mb-6">2. Render Props Pattern</h2>
            <p class="text-lg text-text-secondary leading-relaxed mb-6">
              Render Props is a technique for sharing code between React components using a prop whose value is a function. This pattern is particularly useful for cross-cutting concerns and component logic reuse.
            </p>
            <p class="text-lg text-text-secondary leading-relaxed mb-6">
              Instead of hard-coding what a component renders, you can make it dynamic by passing a function that returns the desired JSX. This gives consumers of your component complete control over what gets rendered while still providing the underlying functionality.
            </p>
            <div class="bg-blue-50 border-l-4 border-blue-500 p-6 my-6 rounded-r-lg">
              <p class="text-blue-800 text-lg">
                <strong>Pro Tip:</strong> Render props work great with custom hooks in modern React applications, providing even more flexibility and reusability. Consider using them together for maximum effect.
              </p>
            </div>
          </section>

          <section class="bg-white/80 backdrop-blur-lg rounded-2xl p-8 border border-white/20 shadow-xl animate-fade-in-scroll">
            <h2 class="text-3xl font-brand-semibold text-text-primary mb-6">3. Custom Hooks</h2>
            <p class="text-lg text-text-secondary leading-relaxed mb-6">
              Custom hooks are perhaps the most powerful pattern in modern React development. They allow you to extract component logic into reusable functions, making your code more modular and testable.
            </p>
            <div class="grid md:grid-cols-2 gap-6 my-8">
              <div class="bg-green-50 p-6 rounded-xl border border-green-200">
                <h4 class="font-brand-semibold text-green-800 text-lg mb-3">Benefits</h4>
                <ul class="text-green-700 leading-relaxed space-y-2">
                  <li>• Encapsulate complex state logic</li>
                  <li>• Share stateful logic between components</li>
                  <li>• Simplify component code</li>
                  <li>• Improve testability</li>
                </ul>
              </div>
              <div class="bg-purple-50 p-6 rounded-xl border border-purple-200">
                <h4 class="font-brand-semibold text-purple-800 text-lg mb-3">Use Cases</h4>
                <ul class="text-purple-700 leading-relaxed space-y-2">
                  <li>• API data fetching</li>
                  <li>• Form validation</li>
                  <li>• Local storage management</li>
                  <li>• Complex state machines</li>
                </ul>
              </div>
            </div>
            <p class="text-lg text-text-secondary leading-relaxed">
              When building enterprise applications, custom hooks become essential for managing complex business logic, API integrations, and state management patterns. They help keep your components focused on rendering while extracting reusable business logic.
            </p>
          </section>

          <section class="bg-white/80 backdrop-blur-lg rounded-2xl p-8 border border-white/20 shadow-xl animate-fade-in-scroll">
            <h2 class="text-3xl font-brand-semibold text-text-primary mb-6">4. Error Boundaries</h2>
            <p class="text-lg text-text-secondary leading-relaxed mb-6">
              Error boundaries are React components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.
            </p>
            <div class="bg-red-50 border border-red-200 rounded-xl p-6 my-6">
              <h4 class="font-brand-semibold text-red-800 text-lg mb-3">Important Note</h4>
              <p class="text-red-700 leading-relaxed">
                Error boundaries only catch errors during rendering, in lifecycle methods, and in constructors of the whole tree below them. They do not catch errors in event handlers, asynchronous code, or during server-side rendering.
              </p>
            </div>
            <p class="text-lg text-text-secondary leading-relaxed">
              In enterprise applications, proper error handling is crucial for user experience and debugging. Error boundaries provide a way to gracefully handle errors and prevent your entire application from crashing when something goes wrong.
            </p>
          </section>
        </div>

        <!-- Conclusion -->
        <div class="bg-gradient-to-r from-accent/10 to-purple-600/10 backdrop-blur-lg rounded-2xl p-8 border border-white/20 shadow-xl mt-12 animate-fade-in-scroll">
          <h2 class="text-3xl font-brand-semibold text-text-primary mb-6">Conclusion</h2>
          <p class="text-lg text-text-secondary leading-relaxed mb-6">
            These advanced React patterns form the foundation of well-architected enterprise applications. By understanding and implementing these patterns, you'll be able to build more maintainable, scalable, and robust React applications that can grow with your business needs.
          </p>
          <p class="text-lg text-text-secondary leading-relaxed">
            Remember, patterns are tools in your toolkit. Use them when they solve real problems in your codebase, not just because they're trendy or new. The best pattern is often the simplest one that solves your specific problem effectively while maintaining code clarity and team productivity.
          </p>
        </div>

        <!-- Tags -->
        <div class="mt-12 pt-8 border-t border-white/20 animate-fade-in-scroll">
          <h3 class="text-xl font-brand-semibold text-text-primary mb-6">Tags</h3>
          <div class="flex flex-wrap gap-3">
            <span class="px-6 py-3 bg-accent/20 text-accent rounded-full text-base font-brand-medium">React</span>
            <span class="px-6 py-3 bg-accent/20 text-accent rounded-full text-base font-brand-medium">JavaScript</span>
            <span class="px-6 py-3 bg-accent/20 text-accent rounded-full text-base font-brand-medium">Enterprise</span>
            <span class="px-6 py-3 bg-accent/20 text-accent rounded-full text-base font-brand-medium">Patterns</span>
            <span class="px-6 py-3 bg-accent/20 text-accent rounded-full text-base font-brand-medium">Frontend</span>
          </div>
        </div>
      </div>
    </article>

    <!-- Suggested Blogs Section - Wider Layout -->
    <section class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-16 pb-16 relative z-10 animate-fade-in-scroll">
      <div class="text-center mb-10">
        <h2 class="text-3xl font-brand-bold text-text-primary mb-4">Suggested Articles</h2>
        <p class="text-lg text-text-secondary">Continue reading with these related articles</p>
      </div>
      
      <!-- Suggested Blog Grid - Full Width -->
      <div class="grid gap-8 lg:grid-cols-3 md:grid-cols-2 grid-cols-1">
        
        <!-- Suggested Blog 1 -->
        <article class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1558655146-d09347e92766?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2064&q=80" 
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
                  src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Mike Chen</p>
                  <p class="text-xs text-text-muted">UI/UX Designer</p>
                </div>
              </div>
              <button class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105">
                Read More
              </button>
            </div>
          </div>
        </article>

        <!-- Suggested Blog 2 -->
        <article class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1517180102446-f3ece451e9d8?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
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
                  src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Alex Rodriguez</p>
                  <p class="text-xs text-text-muted">Vue.js Expert</p>
                </div>
              </div>
              <button class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105">
                Read More
              </button>
            </div>
          </div>
        </article>

        <!-- Suggested Blog 3 -->
        <article class="group bg-white/80 backdrop-blur-lg rounded-2xl shadow-xl border border-white/20 overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          <div class="relative overflow-hidden">
            <img 
              src="https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2155&q=80" 
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
                  src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-4.0.3&ixid=M3wxMJA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=688&q=80" 
                  alt="Author"
                  class="w-10 h-10 rounded-full object-cover ring-2 ring-accent/20"
                />
                <div>
                  <p class="text-sm font-brand-medium text-text-primary">Lisa Thompson</p>
                  <p class="text-xs text-text-muted">CSS Specialist</p>
                </div>
              </div>
              <button class="px-4 py-2 bg-gradient-to-r from-accent to-purple-600 text-white text-sm font-brand-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105">
                Read More
              </button>
            </div>
          </div>
        </article>

      </div>
      
      <!-- Go Back Button -->
       <NuxtLink 
                  to="/blog" >
      <div class="mt-12 text-center" style="margin-bottom: 20px;">
        <button class="px-10 py-4 bg-white/80 backdrop-blur-lg border-2 border-accent text-accent font-brand-semibold rounded-xl hover:bg-accent hover:text-white hover:shadow-xl transition-all duration-300 transform hover:scale-105 inline-flex items-center gap-3 text-lg">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18" />
          </svg>
          Go Back to Articles
        </button>
      </div>
      </NuxtLink>
    </section>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'

// Intersection Observer for scroll animations
onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('animate-visible')
      }
    })
  }, {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
  })

  // Observe all elements with scroll animation classes
  document.querySelectorAll('.animate-fade-in-scroll').forEach(el => {
    observer.observe(el)
  })
})
</script>

<style scoped>
/* Animation Classes */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInDelayed {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fadeInUp 0.8s ease-out forwards;
}

.animate-fade-in-delayed {
  animation: fadeInDelayed 0.8s ease-out forwards;
  animation-delay: 0.3s;
  opacity: 0;
}

.animate-fade-in-scroll {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.animate-fade-in-scroll.animate-visible {
  opacity: 1;
  transform: translateY(0);
}

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
