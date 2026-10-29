<template>
  <div class="min-h-[85vh] flex flex-col font-lexend text-novo-gray">
    <!-- Top Mockup Banner -->
    <div class="w-full h-64 sm:h-80 md:h-[380px] overflow-hidden bg-gray-100">
      <img 
        src="/NE-Mockup1.png" 
        alt="Novo Enviro Architectural Signage" 
        class="w-full h-full object-cover object-[center_35%]"
      />
    </div>

    <!-- Contact Content Section -->
    <div class="max-w-6xl mx-auto px-6 sm:px-8 py-16 md:py-24 w-full">
      <div class="grid grid-cols-1 md:grid-cols-12 gap-12 lg:gap-20">
        
        <!-- Left Column: Heading & Introductory Copy -->
        <div class="md:col-span-7 space-y-6">
          <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium">Get in Touch</p>
          
          <h1 class="font-garamond text-4xl sm:text-5xl md:text-6xl text-novo-gray leading-tight">
            Let's start a <br>
            <span class="italic text-novo-teal">conversation.</span>
          </h1>

          <p class="font-lexend font-light text-novo-gray text-sm md:text-base leading-relaxed pt-2 max-w-xl">
            Whether you're developing a carbon project or seeking certified plastic credits, Novo Enviro brings the expertise, integrity, and innovation to make real climate action happen. <strong class="font-semibold text-novo-gray">Our team responds within 48 hours.</strong>
          </p>
        </div>

        <!-- Right Column: Direct Contact Details -->
        <div class="md:col-span-5 space-y-10 md:pt-4">
          <!-- Email Block -->
          <div class="space-y-2">
            <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium">Email</p>
            <a 
              href="mailto:info@novoenviro.com" 
              class="inline-block font-lexend text-sm md:text-base text-novo-gray hover:text-novo-teal transition-colors font-light">
              info@novoenviro.com
            </a>
          </div>

          <!-- Offices Block -->
          <div class="space-y-2">
            <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium">Offices</p>
            <p class="font-lexend text-sm md:text-base text-novo-gray font-light">
              Sofia, Bulgaria <span class="text-novo-teal mx-1.5">|</span> Istanbul, Türkiye
            </p>
          </div>

          <!-- LinkedIn Block -->
          <div class="space-y-2">
            <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium">Connect</p>
            <a 
              href="https://www.linkedin.com/company/novoenviro/" 
              target="_blank" 
              rel="noopener noreferrer" 
              class="inline-flex items-center space-x-2 text-sm text-novo-gray hover:text-novo-teal transition-colors font-light">
              <Icon name="ph:linkedin-logo-bold" class="text-lg text-novo-teal" />
              <span>Novo Enviro on LinkedIn</span>
            </a>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>