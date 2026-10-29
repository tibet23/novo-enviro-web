<script setup>
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)
const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}
</script>

<template>
  <div class="min-h-screen flex flex-col font-lexend text-novo-gray bg-[#fcfcfc]">
    <!-- Header Navigation -->
    <header class="fixed top-0 w-full bg-white/90 backdrop-blur-md z-50 border-b border-gray-100 transition-all">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-20">
          
          <!-- Full Logo Lockup (Top Left) -->
          <NuxtLink to="/" class="flex-shrink-0 flex items-center" @click="closeMobileMenu">
            <img 
              class="h-10 md:h-11 w-auto object-contain" 
              src="/novo-enviro-logo.svg" 
              alt="Novo Enviro Logo"
            >
          </NuxtLink>

          <!-- Desktop Navigation Links -->
          <nav class="hidden md:flex items-center space-x-8">
            <NuxtLink 
              to="/" 
              class="text-sm font-medium tracking-wide hover:text-novo-teal transition-colors"
              active-class="text-novo-teal font-semibold"
            >
              Home
            </NuxtLink>
            <NuxtLink 
              to="/carbon-credits" 
              class="text-sm font-medium tracking-wide hover:text-novo-teal transition-colors"
              active-class="text-novo-teal font-semibold"
            >
              Carbon Credits
            </NuxtLink>
            <NuxtLink 
              to="/plastic-credits" 
              class="text-sm font-medium tracking-wide hover:text-novo-teal transition-colors"
              active-class="text-novo-teal font-semibold"
            >
              Plastic Credits
            </NuxtLink>
            <NuxtLink 
              to="/careers" 
              class="text-sm font-medium tracking-wide hover:text-novo-teal transition-colors"
              active-class="text-novo-teal font-semibold"
            >
              Careers
            </NuxtLink>
            <NuxtLink 
              to="/contact" 
              class="text-sm font-medium tracking-wide hover:text-novo-teal transition-colors"
              active-class="text-novo-teal font-semibold"
            >
              Contact
            </NuxtLink>
          </nav>

          <!-- Mobile Hamburger Button -->
          <div class="flex items-center md:hidden">
            <button 
              type="button" 
              @click="isMobileMenuOpen = !isMobileMenuOpen"
              class="p-2 rounded-lg text-novo-gray hover:text-novo-teal focus:outline-none"
              aria-label="Toggle Navigation Menu"
            >
              <Icon :name="isMobileMenuOpen ? 'ph:x-bold' : 'ph:list-bold'" class="text-2xl" />
            </button>
          </div>
        </div>
      </div>

      <!-- Mobile Dropdown Menu -->
      <div 
        v-show="isMobileMenuOpen" 
        class="md:hidden bg-white/95 backdrop-blur-xl border-b border-gray-100 px-6 py-6 space-y-4 font-lexend shadow-lg"
      >
        <NuxtLink 
          to="/" 
          @click="closeMobileMenu"
          class="block text-base font-medium hover:text-novo-teal transition-colors"
          active-class="text-novo-teal font-semibold"
        >
          Home
        </NuxtLink>
        <NuxtLink 
          to="/carbon-credits" 
          @click="closeMobileMenu"
          class="block text-base font-medium hover:text-novo-teal transition-colors"
          active-class="text-novo-teal font-semibold"
        >
          Carbon Credits
        </NuxtLink>
        <NuxtLink 
          to="/plastic-credits" 
          @click="closeMobileMenu"
          class="block text-base font-medium hover:text-novo-teal transition-colors"
          active-class="text-novo-teal font-semibold"
        >
          Plastic Credits
        </NuxtLink>
        <NuxtLink 
          to="/careers" 
          @click="closeMobileMenu"
          class="block text-base font-medium hover:text-novo-teal transition-colors"
          active-class="text-novo-teal font-semibold"
        >
          Careers
        </NuxtLink>
        <NuxtLink 
          to="/contact" 
          @click="closeMobileMenu"
          class="block text-base font-medium hover:text-novo-teal transition-colors"
          active-class="text-novo-teal font-semibold"
        >
          Contact
        </NuxtLink>
      </div>
    </header>

    <!-- Main Page Content -->
    <main class="flex-grow pt-20">
      <slot />
    </main>

    <!-- Modern Institutional Multi-Column Footer -->
    <footer class="bg-white border-t border-gray-100 mt-auto">
      <div class="max-w-7xl mx-auto px-6 py-16 lg:py-20">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-12 lg:gap-8">
          
          <!-- Column 1: Brand & Mission (2 cols wide on desktop) -->
          <div class="lg:col-span-2 space-y-6">
            <NuxtLink to="/" class="inline-block">
              <img 
                class="h-10 w-auto object-contain" 
                src="/novo-enviro-logo.svg" 
                alt="Novo Enviro Logo"
              >
            </NuxtLink>
            <p class="font-lexend font-light text-sm text-novo-gray/80 max-w-sm leading-relaxed">
              Offers project development services for high-integrity carbon reduction & carbon removal projects and provides expert consultancy generating internationally certified plastic credits.
            </p>
            <div class="flex items-center space-x-4 pt-2">
              <a 
                href="https://www.linkedin.com/company/novoenviro/" 
                target="_blank" 
                rel="noopener noreferrer"
                class="w-9 h-9 rounded-full bg-gray-50 flex items-center justify-center text-novo-gray hover:bg-novo-teal hover:text-white transition-all duration-300"
                aria-label="LinkedIn"
              >
                <Icon name="ph:linkedin-logo-bold" class="text-lg" />
              </a>
              <a 
                href="mailto:info@novoenviro.com" 
                class="w-9 h-9 rounded-full bg-gray-50 flex items-center justify-center text-novo-gray hover:bg-novo-teal hover:text-white transition-all duration-300"
                aria-label="Email"
              >
                <Icon name="ph:envelope-simple-bold" class="text-lg" />
              </a>
            </div>
          </div>

          <!-- Column 2: Solutions -->
          <div>
            <h4 class="font-lexend text-xs font-semibold uppercase tracking-widest text-novo-teal mb-5">Solutions</h4>
            <ul class="space-y-3 font-lexend text-sm font-light text-novo-gray/80">
              <li>
                <NuxtLink to="/carbon-credits" class="hover:text-novo-teal transition-colors">Carbon Credits</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/plastic-credits" class="hover:text-novo-teal transition-colors">Plastic Credits</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/plastic-credits" class="hover:text-novo-teal transition-colors">Flagship Project</NuxtLink>
              </li>
            </ul>
           </div>

          <!-- Column 3: Company -->
          <div>
            <h4 class="font-lexend text-xs font-semibold uppercase tracking-widest text-novo-teal mb-5">Company</h4>
            <ul class="space-y-3 font-lexend text-sm font-light text-novo-gray/80">
              <li>
                <NuxtLink to="/careers" class="hover:text-novo-teal transition-colors">Careers</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/contact" class="hover:text-novo-teal transition-colors">Contact Us</NuxtLink>
              </li>
            </ul>
          </div>

          <!-- Column 4: Locations -->
          <div>
            <h4 class="font-lexend text-xs font-semibold uppercase tracking-widest text-novo-teal mb-5">Locations</h4>
            <ul class="space-y-3 font-lexend text-sm font-light text-novo-gray/80">
              <li class="flex items-start space-x-2">
                <Icon name="ph:map-pin-duotone" class="text-novo-teal text-base flex-shrink-0 mt-0.5" />
                <span>Sofia, Bulgaria</span>
              </li>
              <li class="flex items-start space-x-2">
                <Icon name="ph:map-pin-duotone" class="text-novo-teal text-base flex-shrink-0 mt-0.5" />
                <span>Istanbul, Türkiye</span>
              </li>
              <li class="pt-2">
                <a href="mailto:info@novoenviro.com" class="text-novo-teal font-medium hover:underline text-xs">
                  info@novoenviro.com
                </a>
              </li>
            </ul>
          </div>

        </div>

        <!-- Bottom Copyright Row -->
        <div class="mt-16 pt-8 border-t border-gray-100 flex items-center justify-center text-xs font-lexend text-novo-gray/60">
          <p>© 2026 Novo Enviro. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>