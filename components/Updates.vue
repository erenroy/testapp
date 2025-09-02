<template>
  <section id="newsletter-section" class="nl-section" ref="sectionRef">
    <div class="nl-container">
      <div class="nl-content-wrapper">
        
        <!-- Left Content - Centered Text Only -->
        <div class="nl-left-content" :class="sectionVisible ? 'nl-fade-in' : ''">
          <div class="nl-badge">Our Newsletter</div>
          <h2 class="nl-title">
            Subscribe Our Newsletter
            <br>
            to Get More Updates
          </h2>
        </div>

        <!-- Right Content - Image Taking Full Height -->
        <div class="nl-right-content" :class="sectionVisible ? 'nl-fade-in-delay' : ''">
          <div class="nl-illustration-wrapper">
            <!-- Image taking full height of section -->
          <img 
  src="https://purepng.com/public/uploads/large/purepng.com-business-womanbusiness-womanbusinesswomanoffice-woman-1421526977603wvxvr.png"
  alt="Woman working on laptop"
  class="nl-main-illustration nl-floating"
  @error="handleImageError"
/>

            
            <!-- Decorative Elements -->
            <div class="nl-decoration-stripes"></div>
            <div class="nl-decoration-dots"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const sectionVisible = ref(false)
const sectionRef = ref(null)

const handleImageError = (event) => {
  event.target.src = 'https://cdni.iconscout.com/illustration/premium/thumb/girl-working-on-laptop-2537387-2146478.png'
}

let observer = null

onMounted(() => {
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          sectionVisible.value = true
        }
      })
    },
    { threshold: 0.2, rootMargin: '0px' }
  )

  if (sectionRef.value) {
    observer.observe(sectionRef.value)
  }
})

onUnmounted(() => {
  if (observer) {
    observer.disconnect()
  }
})
</script>

<style scoped>
/* Section */
.nl-section {
  background: linear-gradient(135deg, #5138ee 0%, #7c3aed 100%);
  overflow: hidden;
  position: relative;
  padding: 3rem 0;
  margin: 2rem 5% 0 5%;
  border-radius: 1.5rem;
  min-height: 320px;
}

.nl-container {
  max-width: 100%;
  margin: 0 auto;
  padding: 0 2rem;
}

.nl-content-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  height: 100%;
}

/* Left content - Centered Text */
.nl-left-content {
  max-width: 28rem;
  margin: 0 auto; /* Center the content */
  text-align: center; /* Center align text */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transform: translateX(-2rem);
  transition: all 1s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.nl-left-content.nl-fade-in {
  opacity: 1;
  transform: translateX(0);
}

.nl-badge {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  color: white;
  padding: 0.375rem 1.25rem;
  border-radius: 9999px;
  font-size: 0.75rem;
  font-weight: 600;
  margin-bottom: 1rem;
  backdrop-filter: blur(10px);
  font-family: 'Poppins', sans-serif;
}

.nl-title {
  font-size: 2.5rem;
  font-weight: 700;
  color: white;
  line-height: 1.2;
  margin-bottom: 0; /* Remove bottom margin since no form below */
  font-family: 'Poppins', sans-serif;
}

/* Right content - Image taking FULL HEIGHT */
.nl-right-content {
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transform: translateX(2rem);
  transition: all 1s cubic-bezier(0.25, 0.46, 0.45, 0.94) 0.3s;
  height: 100%;
}

.nl-right-content.nl-fade-in-delay {
  opacity: 1;
  transform: translateX(0);
}

.nl-illustration-wrapper {
  position: relative;
  width: 100%;
  height: 320px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nl-main-illustration {
  width: auto;
  height: 100%;
  max-width: 400px;
  object-fit: contain;
  z-index: 10;
  filter: drop-shadow(0 8px 16px rgba(0, 0, 0, 0.1));
}

/* Decorative Elements */
.nl-decoration-stripes {
  position: absolute;
  width: 100px;
  height: 60px;
  background: repeating-linear-gradient(
    45deg,
    transparent,
    transparent 3px,
    rgba(34, 211, 238, 0.4) 3px,
    rgba(34, 211, 238, 0.4) 6px
  );
  top: 20px;
  right: 20px;
  border-radius: 12px;
  z-index: 2;
}

.nl-decoration-dots {
  position: absolute;
  width: 60px;
  height: 40px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.4) 1.5px, transparent 1.5px);
  background-size: 12px 12px;
  bottom: 20px;
  left: 20px;
  z-index: 3;
}

/* Floating animation */
.nl-floating {
  animation: nl-float 6s ease-in-out infinite;
}

@keyframes nl-float {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-12px);
  }
}

/* Responsive design */
@media (max-width: 1200px) {
  .nl-section {
    margin-left: 3%;
    margin-right: 3%;
  }
}

@media (max-width: 768px) {
  .nl-section {
    margin-left: 2%;
    margin-right: 2%;
    padding: 2rem 0;
    min-height: 280px;
  }
  
  .nl-content-wrapper {
    grid-template-columns: 1fr;
    gap: 1.5rem;
    text-align: center;
  }
  
  .nl-left-content {
    max-width: 100%;
  }
  
  .nl-title {
    font-size: 2rem;
  }
  
  .nl-illustration-wrapper {
    height: 240px;
  }
}
</style>
