<template>
  <div class="min-h-screen bg-primary">
    <!-- Hero Section with Grid Background -->
    <section class="relative py-24 overflow-hidden">
      <!-- Grid Background -->
      <div class="absolute inset-0 bg-grid-pattern opacity-30"></div>
      
      <!-- Floating Elements -->
      <div class="absolute top-16 left-20 w-3 h-3 bg-accent rounded-full opacity-60"></div>
      <div class="absolute top-32 right-32 w-2 h-2 bg-blue-400 rounded-full opacity-40"></div>
      <div class="absolute bottom-20 left-16 w-4 h-4 bg-pink-400 rounded-full opacity-50"></div>
      
      <div class="relative max-w-6xl mx-auto px-8 text-center">
        <!-- Privacy Policy Pill -->
        <div class="inline-flex items-center px-6 py-3 bg-primary/80 backdrop-blur-sm rounded-full border border-border shadow-sm mb-8">
          <div class="w-2 h-2 bg-accent rounded-full mr-3"></div>
          <span class="text-text-secondary font-brand-medium">Privacy Policy</span>
          <div class="w-2 h-2 bg-accent rounded-full ml-3"></div>
        </div>
        
        <h1 class="text-6xl md:text-7xl font-brand-bold mb-6">
          <span class="text-darker">Your Data</span> 
          <span class="bg-gradient-to-r from-blue-600 via-accent to-purple-600 bg-clip-text text-transparent">Protection</span> 
          <span class="bg-gradient-to-r from-accent to-purple-600 bg-clip-text text-transparent">Matters</span>
          <br />
          <span class="text-darker">Privacy Policy</span>
        </h1>
        
        <p class="text-xl text-text-secondary max-w-4xl mx-auto leading-relaxed">
          Experience complete transparency in data protection with 
          <span class="text-navlink font-brand-semibold">comprehensive privacy controls</span>, 
          <span class="text-navlink font-brand-semibold">secure data handling</span>, and 
          <span class="text-navlink font-brand-semibold">your rights at the center</span> of everything we do.
        </p>
        
        <div class="mt-8 inline-flex items-center px-4 py-2 bg-primary/80 backdrop-blur-sm rounded-lg border border-border shadow-sm">
          <svg class="w-4 h-4 text-accent mr-2" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"/>
          </svg>
          <span class="text-text-muted font-brand-medium">Last updated: January 15, 2025</span>
        </div>
      </div>
    </section>

    <!-- Main Content -->
    <div class="max-w-4xl mx-auto px-8 py-16">
      
      <!-- Introduction -->
      <section class="mb-16">
        <div class="bg-primary rounded-2xl p-8 border border-border shadow-sm">
          <h2 class="text-3xl font-brand-bold text-darker mb-6">Your Privacy is Our Priority</h2>
          <div class="prose prose-lg max-w-none text-text-secondary">
            <p class="mb-4">
              At Station Point, we understand that your privacy is fundamental to your trust in our advanced analytics platform. This comprehensive privacy policy explains in detail how we collect, use, store, and protect your personal information when you use our station intelligence services.
            </p>
            <p class="mb-4">
              We are committed to being transparent about our data practices and ensuring you have complete control over your personal information. This policy applies to all users of our platform, website, and related analytics services, regardless of how you access or use them.
            </p>
            <p>
              By using our station intelligence platform, you acknowledge that you have read and understood this privacy policy. If you do not agree with our practices, please do not use our services.
            </p>
          </div>
        </div>
      </section>

      <!-- Data Collection Overview -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
            </svg>
          </div>
          Information We Collect
        </h2>
        
        <div class="bg-accentlight rounded-2xl p-8 border border-border mb-8">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Account and Profile Information</h3>
            <p class="mb-4">
              When you create an account with our station intelligence platform, we collect information that you voluntarily provide. This includes your name, email address, phone number, company name, job title, and station management role. We also collect any additional information you choose to provide in your profile, such as your professional background, station preferences, and operational requirements.
            </p>
            <p class="mb-6">
              For our premium analytics services, we collect billing information including your payment method details, billing address, and transaction history. However, we do not store your complete payment card information on our servers - this is securely handled by our PCI-DSS compliant payment processors.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Station Data and Analytics Information</h3>
            <p class="mb-4">
              When you use our analytics platform, we automatically collect operational data from your stations, including performance metrics, usage patterns, maintenance schedules, and system diagnostics. This information helps us provide real-time intelligence and predictive analytics for your station operations.
            </p>
            <p class="mb-4">
              We collect device information such as IP addresses, device identifiers, browser types, operating systems, and the specific features you access within our platform. We use cookies, web beacons, and similar tracking technologies to understand how you interact with our analytics tools.
            </p>
            <p>
              Our AI-powered system also processes interaction data about how you use different analytics features, which reports you generate most frequently, what operational insights you access, and how you customize your dashboard. This information is aggregated and analyzed to improve our platform's intelligence capabilities.
            </p>
          </div>
        </div>

        <!-- Data Types Cards -->
        <div class="grid md:grid-cols-3 gap-6">
          <div class="bg-primary rounded-xl p-6 border border-border shadow-sm">
            <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-blue-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-brand-semibold text-navlink mb-2">Personal Data</h3>
            <p class="text-text-secondary text-sm">Contact information, account details, and professional profile data you provide to us.</p>
          </div>

          <div class="bg-primary rounded-xl p-6 border border-border shadow-sm">
            <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M3 3a1 1 0 000 2v8a2 2 0 002 2h2.586l-1.293 1.293a1 1 0 101.414 1.414L10 15.414l2.293 2.293a1 1 0 001.414-1.414L12.414 15H15a2 2 0 002-2V5a1 1 0 100-2H3zm11.707 4.707a1 1 0 00-1.414-1.414L10 9.586 8.707 8.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-brand-semibold text-navlink mb-2">Station Analytics</h3>
            <p class="text-text-secondary text-sm">Operational data, performance metrics, and system diagnostics from your station infrastructure.</p>
          </div>

          <div class="bg-primary rounded-xl p-6 border border-border shadow-sm">
            <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-purple-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M12.395 2.553a1 1 0 00-1.45-.385c-.345.23-.614.558-.822.88-.214.33-.403.713-.57 1.116-.334.804-.614 1.768-.84 2.734a31.365 31.365 0 00-.613 3.58 2.64 2.64 0 01-.945-1.067c-.328-.68-.398-1.534-.398-2.654A1 1 0 005.05 6.05 6.981 6.981 0 003 11a7 7 0 1011.95-4.95c-.592-.591-.98-.985-1.348-1.467-.363-.476-.724-1.063-1.207-2.03zM12.12 15.12A3 3 0 017 13s.879.5 2.5.5c0-1 .5-4 1.25-4.5.5 1 .786 1.293 1.371 1.879A2.99 2.99 0 0113 13a2.99 2.99 0 01-.879 2.121z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-brand-semibold text-navlink mb-2">Usage Intelligence</h3>
            <p class="text-text-secondary text-sm">Platform interaction data, feature usage patterns, and AI-generated insights from your activity.</p>
          </div>
        </div>
      </section>

      <!-- How We Use Your Information -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3z"/>
            </svg>
          </div>
          How We Use Your Information
        </h2>

        <div class="bg-primary rounded-2xl p-8 border border-border shadow-sm mb-8">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <p class="mb-6 text-xl font-brand-medium text-navlink">
              We use your information exclusively to provide, maintain, and improve our station intelligence platform. Here's how we put your data to work for better station management:
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">AI-Powered Analytics and Automation</h3>
            <p class="mb-4">
              Your station data enables our AI algorithms to provide real-time intelligence, predictive maintenance alerts, and automated optimization recommendations. We analyze operational patterns to help you maximize efficiency, reduce downtime, and improve overall station performance.
            </p>
            <p class="mb-6">
              We use machine learning models trained on aggregated, anonymized station data to identify trends, predict potential issues, and generate actionable insights that help you make informed decisions about your station operations.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Platform Personalization and Intelligence</h3>
            <p class="mb-4">
              We use your interaction data to personalize your dashboard, customize alert preferences, and tailor our analytics interface to match your specific station management workflows and operational priorities.
            </p>
            <p class="mb-6">
              Your usage patterns help our platform learn which features are most valuable for different types of station operations, allowing us to prioritize development efforts and create more targeted intelligence tools.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Service Delivery and Support</h3>
            <p class="mb-4">
              We use your contact information to send you critical system alerts, maintenance notifications, platform updates, and changes to our service terms. We also use this information to provide technical support and respond to your platform-related questions.
            </p>
            <p>
              If you opt in to receive our station management insights newsletter, we may send you industry trends, best practices, and new feature announcements that can help optimize your operations. You can opt out of these communications at any time.
            </p>
          </div>
        </div>

        <!-- Usage Purpose Cards -->
        <div class="grid md:grid-cols-2 gap-6">
          <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl p-6 border border-blue-200">
            <div class="w-12 h-12 bg-blue-600 rounded-xl flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M11.3 1.046A1 1 0 0112 2v5h4a1 1 0 01.82 1.573l-7 10A1 1 0 018 18v-5H4a1 1 0 01-.82-1.573l7-10a1 1 0 011.12-.38z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-brand-semibold text-navlink mb-3">Real-Time Intelligence</h3>
            <p class="text-text-secondary">Process your station data to provide instant insights, performance monitoring, and automated alerts for optimal operations.</p>
          </div>

          <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-xl p-6 border border-purple-200">
            <div class="w-12 h-12 bg-purple-600 rounded-xl flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M12.395 2.553a1 1 0 00-1.45-.385c-.345.23-.614.558-.822.88-.214.33-.403.713-.57 1.116-.334.804-.614 1.768-.84 2.734a31.365 31.365 0 00-.613 3.58 2.64 2.64 0 01-.945-1.067c-.328-.68-.398-1.534-.398-2.654A1 1 0 005.05 6.05 6.981 6.981 0 003 11a7 7 0 1011.95-4.95c-.592-.591-.98-.985-1.348-1.467-.363-.476-.724-1.063-1.207-2.03zM12.12 15.12A3 3 0 017 13s.879.5 2.5.5c0-1 .5-4 1.25-4.5.5 1 .786 1.293 1.371 1.879A2.99 2.99 0 0113 13a2.99 2.99 0 01-.879 2.121z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-brand-semibold text-navlink mb-3">Predictive Analytics</h3>
            <p class="text-text-secondary">Use historical patterns and AI algorithms to predict maintenance needs, optimize performance, and prevent operational issues.</p>
          </div>
        </div>
      </section>

      <!-- Data Sharing and Privacy Protection -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z" clip-rule="evenodd"/>
            </svg>
          </div>
          We Never Sell Your Station Data
        </h2>

        <div class="bg-accent rounded-2xl p-8 text-center mb-8">
          <div class="max-w-3xl mx-auto">
            <div class="w-20 h-20 bg-primary rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-10 h-10 text-accent" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M2.166 4.999A11.954 11.954 0 0010 1.944 11.954 11.954 0 0017.834 5c.11.65.166 1.32.166 2.001 0 5.225-3.34 9.67-8 11.317C5.34 16.67 2 12.225 2 7c0-.682.057-1.35.166-2.001zm11.541 3.708a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-3xl font-brand-bold text-primary mb-6">Your Station Data Stays Secure</h3>
            <div class="prose prose-lg max-w-none text-primary opacity-95">
              <p class="mb-4">
                We want to be absolutely clear: we never sell, rent, lease, or trade your station data or personal information to third parties for any purpose. Your operational data and analytics are not commodities to us – they're critical business assets that we protect with the highest security standards.
              </p>
              <p class="mb-6">
                Your station intelligence and operational insights remain exclusively yours. Any data sharing occurs only in very limited circumstances that directly benefit your operations or are required for platform functionality.
              </p>
            </div>
          </div>
        </div>

        <!-- Contact Section -->
        <section class="mb-16">
          <div class="bg-gradient-to-br from-accentlight via-primary to-accentlight rounded-3xl p-12 text-center">
            <div class="w-24 h-24 bg-accent rounded-full flex items-center justify-center mx-auto mb-8">
              <svg class="w-12 h-12 text-primary" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
              </svg>
            </div>
            
            <h2 class="text-4xl font-brand-bold text-darker mb-6">Questions About Your Privacy?</h2>
            <div class="prose prose-lg max-w-none text-text-secondary mb-8">
              <p>
                We're committed to complete transparency about how we handle your station data and personal information. If you have any questions about this privacy policy, want to exercise your privacy rights, or have concerns about data security, our dedicated privacy team is here to help.
              </p>
            </div>
            
            <a href="mailto:privacy@stationpoint.com" 
               class="inline-flex items-center gap-3 px-8 py-4 bg-accent hover:bg-opacity-90 text-primary rounded-xl font-brand-semibold transition-all transform hover:scale-105 shadow-lg">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
              </svg>
              Contact Privacy Team
            </a>
          </div>
        </section>

      </section>

      <!-- Footer -->
      <footer class="border-t border-border pt-12 pb-8">
        <div class="text-center">
          <div class="text-text-muted text-sm font-brand-medium">
            © 2025 Station Point Inc. All rights reserved.
            <span class="mx-2">•</span>
            This privacy policy was last updated on January 15, 2025.
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Privacy Policy - Station Point',
  meta: [
    { name: 'description', content: 'Learn how Station Point protects your privacy and station data. Complete transparency in our data collection, usage, and protection practices.' }
  ]
})
</script>

<style scoped>
.bg-grid-pattern {
  background-image: 
    linear-gradient(rgba(0, 0, 0, 0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0, 0, 0, 0.03) 1px, transparent 1px);
  background-size: 20px 20px;
}
</style>
