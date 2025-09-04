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
        <!-- Terms and Conditions Pill -->
        <div class="inline-flex items-center px-6 py-3 bg-primary/80 backdrop-blur-sm rounded-full border border-border shadow-sm mb-8">
          <div class="w-2 h-2 bg-accent rounded-full mr-3"></div>
          <span class="text-text-secondary font-brand-medium">Terms and Conditions</span>
          <div class="w-2 h-2 bg-accent rounded-full ml-3"></div>
        </div>
        
        <h1 class="text-6xl md:text-7xl font-brand-bold mb-6">
          <span class="text-darker">Service</span> 
          <span class="bg-gradient-to-r from-blue-600 via-accent to-purple-600 bg-clip-text text-transparent">Terms</span> 
          <span class="bg-gradient-to-r from-accent to-purple-600 bg-clip-text text-transparent">Agreement</span>
          <br />
          <span class="text-darker">Terms of Service</span>
        </h1>
        
        <p class="text-xl text-text-secondary max-w-4xl mx-auto leading-relaxed">
          Experience transparent service terms with 
          <span class="text-navlink font-brand-semibold">clear usage guidelines</span>, 
          <span class="text-navlink font-brand-semibold">fair billing practices</span>, and 
          <span class="text-navlink font-brand-semibold">mutual responsibilities</span> for our station intelligence platform.
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
          <h2 class="text-3xl font-brand-bold text-darker mb-6">Welcome to Station Point</h2>
          <div class="prose prose-lg max-w-none text-text-secondary">
            <p class="mb-4">
              These Terms and Conditions ("Terms") govern your access to and use of Station Point's advanced analytics software platform, including all related services, features, and content provided by Station Point Inc. ("we," "us," or "our").
            </p>
            <p class="mb-4">
              By accessing or using our station intelligence platform, you agree to be bound by these Terms. If you disagree with any part of these terms, then you may not access our service.
            </p>
            <p>
              These Terms apply to all visitors, users, and others who access or use our platform, including both free and premium service tiers.
            </p>
          </div>
        </div>
      </section>

      <!-- Service Description -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M3 3a1 1 0 000 2v8a2 2 0 002 2h2.586l-1.293 1.293a1 1 0 101.414 1.414L10 15.414l2.293 2.293a1 1 0 001.414-1.414L12.414 15H15a2 2 0 002-2V5a1 1 0 100-2H3zm11.707 4.707a1 1 0 00-1.414-1.414L10 9.586 8.707 8.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
            </svg>
          </div>
          Our Service
        </h2>
        
        <div class="bg-accentlight rounded-2xl p-8 border border-border mb-8">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Station Intelligence Platform</h3>
            <p class="mb-4">
              Station Point provides a comprehensive analytics platform designed for station management, operational intelligence, and predictive maintenance. Our service includes AI-powered automation, real-time monitoring, performance analytics, and predictive insights for various types of stations and operational facilities.
            </p>
            <p class="mb-6">
              We offer multiple service tiers, including free basic analytics, professional plans with advanced features, and enterprise solutions with custom integrations. All services are provided through our cloud-based platform accessible via web browsers and mobile applications.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Service Availability and Updates</h3>
            <p class="mb-4">
              We strive to maintain 99.9% uptime for our platform, though we cannot guarantee uninterrupted service. We may need to perform maintenance, updates, or modifications to our service, which may temporarily affect availability.
            </p>
            <p class="mb-4">
              We reserve the right to modify, suspend, or discontinue any aspect of our service at any time, with or without notice. We will provide reasonable advance notice for significant changes that materially affect your use of the platform.
            </p>
            <p>
              New features and improvements are regularly added to our platform. Some advanced features may be limited to premium service tiers or require additional subscription fees.
            </p>
          </div>
        </div>

        <!-- Service Features Cards -->
        <div class="grid md:grid-cols-3 gap-6">
          <div class="bg-primary rounded-xl p-6 border border-border shadow-sm">
            <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-blue-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M11.3 1.046A1 1 0 0112 2v5h4a1 1 0 01.82 1.573l-7 10A1 1 0 018 18v-5H4a1 1 0 01-.82-1.573l7-10a1 1 0 011.12-.38z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-brand-semibold text-navlink mb-2">Analytics Platform</h3>
            <p class="text-text-secondary text-sm">Comprehensive station monitoring, performance tracking, and operational intelligence tools.</p>
          </div>

          <div class="bg-primary rounded-xl p-6 border border-border shadow-sm">
            <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M12.395 2.553a1 1 0 00-1.45-.385c-.345.23-.614.558-.822.88-.214.33-.403.713-.57 1.116-.334.804-.614 1.768-.84 2.734a31.365 31.365 0 00-.613 3.58 2.64 2.64 0 01-.945-1.067c-.328-.68-.398-1.534-.398-2.654A1 1 0 005.05 6.05 6.981 6.981 0 003 11a7 7 0 1011.95-4.95c-.592-.591-.98-.985-1.348-1.467-.363-.476-.724-1.063-1.207-2.03zM12.12 15.12A3 3 0 017 13s.879.5 2.5.5c0-1 .5-4 1.25-4.5.5 1 .786 1.293 1.371 1.879A2.99 2.99 0 0113 13a2.99 2.99 0 01-.879 2.121z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-brand-semibold text-navlink mb-2">AI-Powered Insights</h3>
            <p class="text-text-secondary text-sm">Machine learning algorithms that provide predictive maintenance and optimization recommendations.</p>
          </div>

          <div class="bg-primary rounded-xl p-6 border border-border shadow-sm">
            <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-purple-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M2.166 4.999A11.954 11.954 0 0010 1.944 11.954 11.954 0 0017.834 5c.11.65.166 1.32.166 2.001 0 5.225-3.34 9.67-8 11.317C5.34 16.67 2 12.225 2 7c0-.682.057-1.35.166-2.001zm11.541 3.708a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-lg font-brand-semibold text-navlink mb-2">Real-Time Monitoring</h3>
            <p class="text-text-secondary text-sm">Live data streams, automated alerts, and continuous monitoring of your station operations.</p>
          </div>
        </div>
      </section>

      <!-- User Accounts and Responsibilities -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
            </svg>
          </div>
          User Accounts and Responsibilities
        </h2>

        <div class="bg-primary rounded-2xl p-8 border border-border shadow-sm mb-8">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Account Creation and Security</h3>
            <p class="mb-4">
              To access our platform, you must create an account with accurate, complete, and current information. You are responsible for maintaining the confidentiality of your account credentials and for all activities that occur under your account.
            </p>
            <p class="mb-6">
              You must immediately notify us of any unauthorized use of your account or any other breach of security. We will not be liable for any loss or damage arising from your failure to comply with these security obligations.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Acceptable Use</h3>
            <p class="mb-4">
              You agree to use our service only for lawful purposes and in accordance with these Terms. You may not use our platform to:
            </p>
            <ul class="mb-4 space-y-2">
              <li>• Violate any applicable laws or regulations</li>
              <li>• Infringe on the rights of others</li>
              <li>• Attempt to gain unauthorized access to our systems</li>
              <li>• Interfere with or disrupt our service or servers</li>
              <li>• Use our platform for any commercial purpose without authorization</li>
              <li>• Upload malicious code, viruses, or harmful content</li>
              <li>• Share your account credentials with unauthorized parties</li>
            </ul>
            <p>
              We reserve the right to investigate and take appropriate legal action against anyone who violates these provisions, including suspending or terminating their account without notice.
            </p>
          </div>
        </div>

        <!-- Responsibility Cards -->
        <div class="grid md:grid-cols-2 gap-6">
          <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-xl p-6 border border-green-200">
            <div class="w-12 h-12 bg-green-600 rounded-xl flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-brand-semibold text-navlink mb-3">Your Responsibilities</h3>
            <p class="text-text-secondary">Maintain account security, provide accurate information, and use the platform in compliance with our terms and applicable laws.</p>
          </div>

          <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl p-6 border border-blue-200">
            <div class="w-12 h-12 bg-blue-600 rounded-xl flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M2.166 4.999A11.954 11.954 0 0010 1.944 11.954 11.954 0 0017.834 5c.11.65.166 1.32.166 2.001 0 5.225-3.34 9.67-8 11.317C5.34 16.67 2 12.225 2 7c0-.682.057-1.35.166-2.001zm11.541 3.708a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-xl font-brand-semibold text-navlink mb-3">Our Responsibilities</h3>
            <p class="text-text-secondary">Provide reliable service, protect your data, maintain platform security, and offer customer support for your station intelligence needs.</p>
          </div>
        </div>
      </section>

      <!-- Billing and Payments -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path d="M4 4a2 2 0 00-2 2v1h16V6a2 2 0 00-2-2H4z"/>
              <path fill-rule="evenodd" d="M18 9H2v5a2 2 0 002 2h12a2 2 0 002-2V9zM4 13a1 1 0 011-1h1a1 1 0 110 2H5a1 1 0 01-1-1zm5-1a1 1 0 100 2h1a1 1 0 100-2H9z" clip-rule="evenodd"/>
            </svg>
          </div>
          Billing and Payments
        </h2>

        <div class="bg-accentlight rounded-2xl p-8 border border-border">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Subscription Plans and Pricing</h3>
            <p class="mb-4">
              We offer multiple subscription tiers for our station intelligence platform, including free basic access, professional plans, and enterprise solutions. Current pricing is available on our website and may be updated from time to time with reasonable notice.
            </p>
            <p class="mb-6">
              Subscription fees are billed in advance on a monthly or annual basis, depending on your chosen plan. All fees are non-refundable except as expressly stated in our refund policy or as required by applicable law.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Payment Terms</h3>
            <p class="mb-4">
              Payment is due at the beginning of each billing cycle. If payment fails, we will attempt to charge your payment method again. If payment continues to fail, we may suspend or terminate your access to paid features after providing reasonable notice.
            </p>
            <p class="mb-6">
              You are responsible for providing current, complete, and accurate billing information and for updating this information if it changes. All fees are exclusive of applicable taxes, which you are responsible for paying.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Cancellation and Refunds</h3>
            <p class="mb-4">
              You may cancel your subscription at any time through your account settings. Cancellation will take effect at the end of your current billing period, and you will retain access to paid features until that time.
            </p>
            <p>
              We offer a 30-day money-back guarantee for new premium subscriptions. If you cancel within 30 days of your initial subscription, we will provide a full refund of your first payment.
            </p>
          </div>
        </div>
      </section>

      <!-- Intellectual Property -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M12.395 2.553a1 1 0 00-1.45-.385c-.345.23-.614.558-.822.88-.214.33-.403.713-.57 1.116-.334.804-.614 1.768-.84 2.734a31.365 31.365 0 00-.613 3.58 2.64 2.64 0 01-.945-1.067c-.328-.68-.398-1.534-.398-2.654A1 1 0 005.05 6.05 6.981 6.981 0 003 11a7 7 0 1011.95-4.95c-.592-.591-.98-.985-1.348-1.467-.363-.476-.724-1.063-1.207-2.03zM12.12 15.12A3 3 0 017 13s.879.5 2.5.5c0-1 .5-4 1.25-4.5.5 1 .786 1.293 1.371 1.879A2.99 2.99 0 0113 13a2.99 2.99 0 01-.879 2.121z" clip-rule="evenodd"/>
            </svg>
          </div>
          Intellectual Property Rights
        </h2>

        <div class="bg-primary rounded-2xl p-8 border border-border shadow-sm">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Our Intellectual Property</h3>
            <p class="mb-4">
              The Station Point platform, including all software, analytics algorithms, user interfaces, content, and documentation, is owned by Station Point Inc. and protected by copyright, trademark, and other intellectual property laws.
            </p>
            <p class="mb-6">
              We grant you a limited, non-exclusive, non-transferable license to access and use our platform solely for your internal business purposes in accordance with these Terms. This license does not include any rights to modify, distribute, or create derivative works.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Your Data and Content</h3>
            <p class="mb-4">
              You retain all rights to the data and content you upload to our platform. By using our service, you grant us a limited license to process, analyze, and display your data solely for the purpose of providing our analytics services to you.
            </p>
            <p class="mb-6">
              We may use aggregated, anonymized data derived from your usage to improve our platform and develop new features, but we will never share your specific operational data or personally identifiable information without your consent.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Respect for Third-Party Rights</h3>
            <p>
              You warrant that you have all necessary rights to the data and content you provide to our platform and that your use of our service does not infringe on the intellectual property rights of any third party.
            </p>
          </div>
        </div>
      </section>

      <!-- Limitation of Liability -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z" clip-rule="evenodd"/>
            </svg>
          </div>
          Disclaimers and Limitation of Liability
        </h2>

        <div class="bg-accent rounded-2xl p-8 text-center mb-8">
          <div class="max-w-3xl mx-auto">
            <div class="w-20 h-20 bg-primary rounded-full flex items-center justify-center mx-auto mb-6">
              <svg class="w-10 h-10 text-accent" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M8.257 3.099c.765-1.36 2.722-1.36 3.486 0l5.58 9.92c.75 1.334-.213 2.98-1.742 2.98H4.42c-1.53 0-2.493-1.646-1.743-2.98l5.58-9.92zM11 13a1 1 0 11-2 0 1 1 0 012 0zm-1-8a1 1 0 00-1 1v3a1 1 0 002 0V6a1 1 0 00-1-1z" clip-rule="evenodd"/>
              </svg>
            </div>
            <h3 class="text-3xl font-brand-bold text-primary mb-6">Service Disclaimers</h3>
            <div class="prose prose-lg max-w-none text-primary opacity-95">
              <p class="mb-4">
                Our station intelligence platform is provided "as is" without warranties of any kind. While we strive for accuracy and reliability, we cannot guarantee that our analytics and predictions will be error-free or suitable for all operational decisions.
              </p>
              <p>
                You acknowledge that station management involves inherent risks and that our platform is a tool to assist decision-making, not replace professional judgment and expertise.
              </p>
            </div>
          </div>
        </div>

        <div class="bg-primary rounded-2xl p-8 border border-border shadow-sm">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Limitation of Liability</h3>
            <p class="mb-4">
              To the maximum extent permitted by law, Station Point Inc. shall not be liable for any indirect, incidental, special, consequential, or punitive damages, including but not limited to loss of profits, data, or business opportunities, arising from your use of our platform.
            </p>
            <p class="mb-6">
              Our total liability for any claims arising from these Terms or your use of our service shall not exceed the amount you paid us in the twelve months preceding the claim, or $100, whichever is greater.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Indemnification</h3>
            <p>
              You agree to indemnify and hold harmless Station Point Inc. from any claims, damages, or expenses arising from your use of our platform, your violation of these Terms, or your infringement of any third-party rights.
            </p>
          </div>
        </div>
      </section>

      <!-- Termination -->
      <section class="mb-16">
        <h2 class="text-4xl font-brand-bold text-darker mb-8 flex items-center gap-4">
          <div class="w-12 h-12 bg-accent rounded-xl flex items-center justify-center">
            <svg class="w-6 h-6 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"/>
            </svg>
          </div>
          Termination
        </h2>

        <div class="bg-accentlight rounded-2xl p-8 border border-border">
          <div class="prose prose-lg max-w-none text-text-secondary">
            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Termination by You</h3>
            <p class="mb-6">
              You may terminate your account and stop using our service at any time. Upon termination, your access to the platform will cease, but these Terms will continue to apply to your prior use of the service.
            </p>

            <h3 class="text-2xl font-brand-semibold text-navlink mb-4">Termination by Us</h3>
            <p class="mb-4">
              We may suspend or terminate your account if you violate these Terms, fail to pay fees when due, or engage in activities that harm our platform or other users. We will provide reasonable notice before termination unless immediate action is required for security reasons.
            </p>
            <p>
              Upon termination, you will lose access to your account and any data stored on our platform. We recommend regularly backing up your important data to ensure you retain access to it.
            </p>
          </div>
        </div>
      </section>

      <!-- Contact Section -->
      <section class="mb-16">
        <div class="bg-gradient-to-br from-accentlight via-primary to-accentlight rounded-3xl p-12 text-center">
          <div class="w-24 h-24 bg-accent rounded-full flex items-center justify-center mx-auto mb-8">
            <svg class="w-12 h-12 text-primary" fill="currentColor" viewBox="0 0 20 20">
              <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
              <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
            </svg>
          </div>
          
          <h2 class="text-4xl font-brand-bold text-darker mb-6">Questions About These Terms?</h2>
          <div class="prose prose-lg max-w-none text-text-secondary mb-8">
            <p>
              We're here to help you understand our terms and conditions. If you have any questions about these Terms, need clarification on our policies, or want to discuss your specific use case, our legal and support teams are ready to assist you.
            </p>
          </div>
          
          <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
            <a href="mailto:legal@stationpoint.com" 
               class="inline-flex items-center gap-3 px-8 py-4 bg-accent hover:bg-opacity-90 text-primary rounded-xl font-brand-semibold transition-all transform hover:scale-105 shadow-lg">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
              </svg>
              Contact Legal Team
            </a>
            
            <a href="mailto:support@stationpoint.com" 
               class="inline-flex items-center gap-3 px-8 py-4 bg-primary hover:bg-accentlight text-accent border border-accent rounded-xl font-brand-semibold transition-all">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z" clip-rule="evenodd"/>
              </svg>
              Get Support
            </a>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <footer class="border-t border-border pt-12 pb-8">
        <div class="text-center">
          <div class="text-text-muted text-sm font-brand-medium">
            © 2025 Station Point Inc. All rights reserved.
            <span class="mx-2">•</span>
            These terms and conditions were last updated on January 15, 2025.
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Terms and Conditions - Station Point',
  meta: [
    { name: 'description', content: 'Read Station Point\'s terms and conditions for our station intelligence platform. Clear guidelines for service usage, billing, and user responsibilities.' }
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
