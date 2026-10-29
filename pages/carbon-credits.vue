<script setup>
import { ref, onMounted } from 'vue'

const isLoaded = ref(false)

onMounted(() => {
  setTimeout(() => {
    isLoaded.value = true
  }, 100)
})
</script>

<template>
  <div class="space-y-24 py-16">
    <!-- Hero / Header Section -->
    <section class="max-w-4xl mx-auto px-4 text-center">
      <!-- Title & Category Cascade -->
      <div 
        class="transition-all duration-1000 ease-out"
        :class="isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'">
        <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-6">Project Development</p>
        <h1 class="font-garamond text-5xl md:text-6xl text-novo-gray mb-2">High-Integrity</h1>
        <h2 class="font-garamond italic text-5xl md:text-6xl text-novo-teal mb-8">Carbon Credits.</h2>
      </div>
      
      <!-- Expanding Centered Teal Line -->
      <div 
        class="h-[2px] bg-novo-teal mx-auto mb-8 transition-all duration-1000 delay-300 ease-out"
        :class="isLoaded ? 'w-12 opacity-100' : 'w-0 opacity-0'">
      </div>

      <!-- Narrative Text Fade-In -->
      <p 
        class="font-lexend font-light text-novo-gray text-sm md:text-base leading-relaxed max-w-3xl mx-auto transition-all duration-1000 delay-200 ease-out"
        :class="isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'">
        There is no denying the importance of verified carbon credits in the fight against global warming. Novo Enviro develops <strong class="font-semibold text-novo-gray">carbon reduction and removal projects</strong> certified under internationally recognized standards. Every credit we bring to market satisfies quality criteria and is independently verified. We don't compromise on the fundamentals.
      </p>
    </section>

    <!-- CTA Button 1 -->
    <section class="py-8 flex justify-center">
      <NuxtLink 
        to="/contact" 
        class="inline-flex items-center gap-2.5 px-7 py-3.5 bg-novo-teal text-white rounded-full font-lexend text-sm font-semibold hover:bg-novo-gray hover:shadow-lg transition-all duration-300">
        <span>Start a Project</span>
        <Icon name="ph:paper-plane-tilt-fill" class="text-base" />
      </NuxtLink>
    </section>

    <!-- What Are Carbon Credits Section -->
    <section class="max-w-4xl mx-auto px-4">
      <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-6">What Are Carbon Credits</p>
      <div class="font-garamond text-4xl md:text-5xl text-novo-gray leading-tight mb-8">
        <p>The instrument. The mechanism. <span class="italic text-novo-teal">The value.</span></p>
      </div>

      <div class="space-y-6 font-lexend text-novo-gray text-sm md:text-base leading-relaxed">
        <p class="italic text-novo-gray/80">
          "One carbon credit represents the verified reduction or removal of one metric tonne of CO₂ equivalent — independently confirmed by an accredited third party."
        </p>
        <p class="font-light">
          Carbon credits enable corporations to address unavoidable emissions by funding projects that generate an equivalent volume of verified greenhouse gas reductions. A credit is issued only after an independent Validation and Verification Body (VVB) confirms the reduction has occurred in line with the relevant standard's methodology.
        </p>
        <p class="font-light">
          Novo Enviro develops <strong class="font-semibold text-novo-gray">Verified Emission Reductions (VERs)</strong> — produced by projects fully compliant with internationally recognised verification standards. VERs are registered on public registries, ensuring full traceability and preventing double counting.
        </p>
        <p class="font-light">
          <strong class="font-semibold text-novo-gray">For institutional buyers</strong>, high-quality carbon credits are critical instruments for net-zero strategy. They provide funding for accelerating carbon reductions and removals that would not have occurred otherwise.
        </p>
      </div>
    </section>

    <!-- Project Portfolio Section -->
    <section class="max-w-5xl mx-auto px-4">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div>
          <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-4">Project Portfolio</p>
          <h2 class="font-garamond text-4xl text-novo-gray mb-6 leading-tight">
            Carbon reduction &amp;<br>
            removal <span class="italic text-novo-teal">project types.</span>
          </h2>
          <div class="space-y-4 font-lexend font-light text-novo-gray text-sm leading-relaxed">
            <p>
              There are several types of projects that generate carbon offset credits. Some type of carbon offset projects are; renewable energy, energy efficiency, agriculture, forestry, waste management and handling, methane capture and fuel switch.
            </p>
            <p>
              These projects must adhere to international criteria that have been independently verified and have a measurable positive impact on society, the environment, and the economy—all of which support sustainable development.
            </p>
          </div>
        </div>
        <div class="flex justify-center">
          <img 
            src="/carbon-types.png" 
            alt="Carbon reduction and removal project types diagram" 
            class="max-w-full h-auto object-contain"
          />
        </div>
      </div>
    </section>

    <!-- Six Pillars Section -->
    <section class="max-w-5xl mx-auto px-4">
      <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-4">Carbon Credit Quality</p>
      <h2 class="font-garamond text-4xl md:text-5xl text-novo-gray leading-tight">Six Pillars.</h2>
      <h3 class="font-garamond italic text-4xl md:text-5xl text-novo-teal mb-6">Zero <span class="not-italic text-novo-gray">Compromise.</span></h3>
      
      <p class="font-lexend font-light text-novo-gray text-sm md:text-base mb-12">
        Every carbon project we develop is built on six non-negotiable quality criteria. <strong class="font-semibold">This is the architecture of every project we build.</strong>
      </p>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 font-lexend">
        <div class="bg-novo-teal/15 text-novo-gray p-6 rounded-2xl border-2 border-white shadow-sm hover:shadow-md transition-shadow">
          <p class="text-novo-teal text-xs font-mono font-medium mb-2">01</p>
          <h4 class="font-medium text-base mb-2">Verifiability</h4>
          <p class="text-xs font-light leading-relaxed text-novo-gray/80">A thorough audit trail documenting how the project delivered on its objectives and was verifiably feasible.</p>
        </div>

        <div class="bg-novo-teal/15 text-novo-gray p-6 rounded-2xl border-2 border-white shadow-sm hover:shadow-md transition-shadow">
          <p class="text-novo-teal text-xs font-mono font-medium mb-2">02</p>
          <h4 class="font-medium text-base mb-2">Realness</h4>
          <p class="text-xs font-light leading-relaxed text-novo-gray/80">Emission reductions are measurable, independently quantifiable, and supported by verifiable monitoring data.</p>
        </div>

        <div class="bg-novo-teal/15 text-novo-gray p-6 rounded-2xl border-2 border-white shadow-sm hover:shadow-md transition-shadow">
          <p class="text-novo-teal text-xs font-mono font-medium mb-2">03</p>
          <h4 class="font-medium text-base mb-2">Permanence</h4>
          <p class="text-xs font-light leading-relaxed text-novo-gray/80">Over time, the project achieves the promised carbon reductions in a sustained manner.</p>
        </div>

        <div class="bg-novo-teal/15 text-novo-gray p-6 rounded-2xl border-2 border-white shadow-sm hover:shadow-md transition-shadow">
          <p class="text-novo-teal text-xs font-mono font-medium mb-2">04</p>
          <h4 class="font-medium text-base mb-2">Additionality</h4>
          <p class="text-xs font-light leading-relaxed text-novo-gray/80">The project activity would not have occurred under a business-as-usual scenario without the financial incentive created by carbon credit revenues.</p>
        </div>

        <div class="bg-novo-teal/15 text-novo-gray p-6 rounded-2xl border-2 border-white shadow-sm hover:shadow-md transition-shadow">
          <p class="text-novo-teal text-xs font-mono font-medium mb-2">05</p>
          <h4 class="font-medium text-base mb-2">No Leakage</h4>
          <p class="text-xs font-light leading-relaxed text-novo-gray/80">The project's emissions reduction does not cause additional emissions to be produced elsewhere.</p>
        </div>

        <div class="bg-novo-teal/15 text-novo-gray p-6 rounded-2xl border-2 border-white shadow-sm hover:shadow-md transition-shadow">
          <p class="text-novo-teal text-xs font-mono font-medium mb-2">06</p>
          <h4 class="font-medium text-base mb-2">No Double Counting</h4>
          <p class="text-xs font-light leading-relaxed text-novo-gray/80">One tonne of CO₂ reduced or removed generates one credit, claimed by one beneficial owner.</p>
        </div>
      </div>
    </section>

    <!-- Bottom Call To Action -->
    <section class="text-center pt-8 pb-12">
      <h2 class="font-garamond text-4xl md:text-5xl text-novo-gray mb-2">Ready to develop a</h2>
      <h3 class="font-garamond italic text-4xl md:text-5xl text-novo-teal mb-10">carbon project?</h3>
      
      <div class="flex justify-center">
        <NuxtLink 
          to="/contact" 
          class="inline-flex items-center gap-2.5 px-7 py-3.5 bg-novo-teal text-white rounded-full font-lexend text-sm font-semibold hover:bg-novo-gray hover:shadow-lg transition-all duration-300">
          <span>Contact Novo Enviro</span>
          <Icon name="ph:paper-plane-tilt-fill" class="text-base" />
        </NuxtLink>
      </div>
    </section>
  </div>
</template>