<script setup>
import { ref, onMounted } from 'vue'

// Trigger animations on load
const isLoaded = ref(false)
onMounted(() => {
  setTimeout(() => {
    isLoaded.value = true
  }, 100)
})

const accordions = ref([
  { title: 'Expertise', content: 'We bring a wealth of experience to the table. Our team is comprised of passionate professionals with a deep understanding of carbon project development, plastic waste management, and the responsible trade of environmental assets. A thorough understanding of what buyers, regulators, and standard bodies require. Seven years of carbon market experience. Over three million credits traded and contracted. More than five projects validated under the world\'s leading standard bodies.', open: false },
  { title: 'Integrity', content: 'We believe in building trust through transparency and ethical practices. Every project we undertake adheres to the highest standards, ensuring measurable environmental benefits.', open: false },
  { title: 'Flexibility', content: 'We recognize that there\'s no one-size-fits-all solution to sustainability issues. We approach each project with a creative mindset, tailoring our strategies to meet your specific needs and goals.', open: false },
  { title: 'Innovation', content: 'Our commitment to innovation ensures that the solutions we offer are not only effective today, but also adaptable to meet the evolving challenges of tomorrow.', open: false }
])

const toggleAccordion = (index) => {
  accordions.value[index].open = !accordions.value[index].open
}
</script>

<template>
  <div class="overflow-hidden">
    <!-- Cinematic Hero Section -->
    <section class="relative h-[90vh] flex items-center justify-center overflow-hidden bg-[#fcfcfc]">
      <!-- Slow Pan Background Image -->
      <div 
        class="absolute inset-0 bg-cover bg-center transition-transform duration-[20000ms] ease-out"
        :class="isLoaded ? 'scale-110' : 'scale-100'"
        style="background-image: url('/intro-clouds.jpg');">
      </div>
      <!-- Subtle white wash overlay for text readability -->
      <div class="absolute inset-0 bg-white/40"></div>
      
      <!-- Float-up Intro Content -->
      <div 
        class="relative z-10 py-20 px-4 max-w-5xl mx-auto text-center transition-all duration-[1500ms] ease-out delay-300"
        :class="isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'">
        <h1 class="font-garamond text-6xl md:text-7xl lg:text-8xl text-novo-gray mb-6 leading-tight">
          Where Capital Meets <br>
          <span class="text-novo-teal italic">Climate</span> Integrity.
        </h1>
        <div class="w-12 h-[2px] bg-novo-teal mx-auto mb-8"></div>
        <p class="font-lexend font-light text-lg md:text-xl leading-relaxed text-novo-gray max-w-3xl mx-auto">
          Novo Enviro offers project development services for <strong class="font-medium text-novo-gray">high-integrity carbon reduction & carbon removal projects</strong> and provides expert consultancy generating <strong class="font-medium text-novo-gray">internationally certified plastic credits.</strong>
        </p>
      </div>
    </section>

    <!-- Glassmorphism Stats & Quote -->
    <section class="py-24 px-4 bg-[#fcfcfc] relative -mt-20 z-20">
      <div class="max-w-6xl mx-auto grid md:grid-cols-12 gap-12 items-center">
        <div class="md:col-span-7">
          <p class="font-lexend font-light italic text-3xl md:text-4xl text-novo-gray leading-snug">
            "<strong class="font-medium">Action on climate change is essential to</strong> <span class="text-novo-teal font-medium not-italic">achieve net-zero.</span>"
          </p>
        </div>
        
        <!-- Glass Cards for Stats -->
        <div class="md:col-span-5 space-y-6">
          <div class="flex items-center space-x-6 p-6 bg-white/70 backdrop-blur-md rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow duration-500">
            <Icon name="ph:chart-line-up-duotone" class="text-5xl text-novo-teal flex-shrink-0" />
            <div>
              <p class="font-garamond text-4xl font-bold text-novo-gray">3M<span class="text-novo-teal">+</span></p>
              <p class="font-lexend text-xs font-light tracking-widest uppercase text-gray-500 mt-1">Credits Traded</p>
            </div>
          </div>
          
          <div class="flex items-center space-x-6 p-6 bg-white/70 backdrop-blur-md rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow duration-500">
            <Icon name="ph:clock-duotone" class="text-5xl text-novo-teal flex-shrink-0" />
            <div>
              <p class="font-garamond text-4xl font-bold text-novo-gray">7<span class="text-novo-teal">+ yrs</span></p>
              <p class="font-lexend text-xs font-light tracking-widest uppercase text-gray-500 mt-1">Markets Experience</p>
            </div>
          </div>

          <div class="flex items-center space-x-6 p-6 bg-white/70 backdrop-blur-md rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow duration-500">
            <Icon name="ph:seal-check-duotone" class="text-5xl text-novo-teal flex-shrink-0" />
            <div>
              <p class="font-garamond text-4xl font-bold text-novo-gray">5<span class="text-novo-teal">+</span></p>
              <p class="font-lexend text-xs font-light tracking-widest uppercase text-gray-500 mt-1">Projects Validated</p>
              <p class="font-lexend text-[10px] text-gray-400 mt-1">VERRA | GOLD STANDARD | PPRS</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Overlapping Solutions Section -->
    <section class="py-32 px-4 max-w-7xl mx-auto">
      <div class="text-center mb-24">
        <p class="text-novo-teal tracking-[0.3em] uppercase text-xs font-medium mb-4">Our Climate Solutions</p>
        <h2 class="font-garamond text-5xl md:text-6xl text-novo-gray">
          Two Pathways<br>to <span class="text-novo-teal italic">Real</span> Impact.
        </h2>
      </div>

      <div class="space-y-32">
        <!-- Carbon Overlap -->
        <div class="relative flex flex-col md:flex-row items-center group">
          <div class="md:w-3/5 relative overflow-hidden rounded-2xl shadow-xl z-10 transition-transform duration-700 group-hover:scale-[1.02]">
            <div class="absolute inset-0 bg-novo-teal/10 group-hover:bg-transparent transition-colors duration-700 z-10"></div>
            <!-- Updated path for Carbon Project Development image -->
            <img src="/carbon-projects-pic.jpg" alt="Carbon Project Development" class="w-full h-96 object-cover">
          </div>
          <div class="md:w-1/2 md:-ml-24 mt-8 md:mt-0 relative z-20 bg-white/90 backdrop-blur-xl p-10 md:p-14 rounded-2xl shadow-2xl border border-gray-50">
            <Icon name="ph:leaf-duotone" class="text-4xl text-novo-teal mb-6" />
            <h3 class="font-garamond text-4xl text-novo-gray mb-4">Carbon Project <span class="italic text-novo-teal">Development</span></h3>
            <p class="font-lexend font-light text-novo-gray/80 leading-relaxed mb-8">Developing impactful carbon reduction and removal projects that generate high-quality credits to help organizations realize their net-zero commitments. You get credits you can actually stand behind.</p>
            <NuxtLink to="/carbon-credits" class="inline-flex items-center space-x-2 font-lexend font-medium text-novo-teal hover:text-novo-gray transition-colors">
              <span>Explore Carbon Credits</span>
              <Icon name="ph:arrow-right" class="text-lg" />
            </NuxtLink>
          </div>
        </div>

        <!-- Plastic Overlap (Reversed) -->
        <div class="relative flex flex-col md:flex-row-reverse items-center group">
          <div class="md:w-3/5 relative overflow-hidden rounded-2xl shadow-xl z-10 transition-transform duration-700 group-hover:scale-[1.02]">
            <div class="absolute inset-0 bg-novo-teal/10 group-hover:bg-transparent transition-colors duration-700 z-10"></div>
            <!-- Updated path for Plastic Credit Consultancy image -->
            <img src="/plastic-projects-pic.jpg" alt="Plastic Credit Consultancy" class="w-full h-96 object-cover">
          </div>
          <div class="md:w-1/2 md:-mr-24 mt-8 md:mt-0 relative z-20 bg-white/90 backdrop-blur-xl p-10 md:p-14 rounded-2xl shadow-2xl border border-gray-50">
            <Icon name="ph:recycle-duotone" class="text-4xl text-novo-teal mb-6" />
            <h3 class="font-garamond text-4xl text-novo-gray mb-4">Plastic Credit <span class="italic text-novo-teal">Consultancy</span></h3>
            <p class="font-lexend font-light text-novo-gray/80 leading-relaxed mb-8">Turn plastic waste into positive change. We advise plastic recycling operations on earning internationally certified plastic credits. Develop high-impact plastic credit projects with us for a sustainable future.</p>
            <NuxtLink to="/plastic-credits" class="inline-flex items-center space-x-2 font-lexend font-medium text-novo-teal hover:text-novo-gray transition-colors">
              <span>Explore Plastic Credits</span>
              <Icon name="ph:arrow-right" class="text-lg" />
            </NuxtLink>
          </div>
        </div>
      </div>
    </section>

    <!-- Modern Interactive Accordion -->
    <section class="py-32 px-4 bg-[#fcfcfc] text-novo-gray">
      <div class="max-w-4xl mx-auto grid md:grid-cols-12 gap-16">
        <div class="md:col-span-5 md:sticky top-32 h-fit">
          <p class="text-novo-teal tracking-[0.3em] uppercase text-xs font-medium mb-4">Why Novo Enviro</p>
          <h2 class="font-garamond text-5xl mb-6 leading-tight">
            Expertise You Can<br>
            <span class="text-novo-teal italic">Verify. Trust.<br>Rely On.</span>
          </h2>
          <p class="font-lexend font-light text-novo-gray/80 leading-relaxed">
            We operate at the frontier of climate finance, developing verifiable, certified environmental assets for a sustainable future.
          </p>
        </div>

        <div class="md:col-span-7 space-y-2">
          <div 
            v-for="(item, index) in accordions" :key="index" 
            class="border-b border-gray-200 overflow-hidden transition-all duration-300">
            <button 
              @click="toggleAccordion(index)" 
              class="w-full py-6 flex justify-between items-center text-left focus:outline-none group">
              <span class="font-garamond text-3xl group-hover:text-novo-teal transition-colors" :class="item.open ? 'text-novo-teal' : 'text-novo-gray'">
                {{ item.title }}
              </span>
              <Icon 
                name="ph:caret-down-duotone" 
                class="text-2xl transition-transform duration-500 ease-out" 
                :class="item.open ? 'rotate-180 text-novo-teal' : 'text-novo-gray/40 group-hover:text-novo-teal'" 
              />
            </button>
            <div 
              class="font-lexend font-light text-novo-gray/80 leading-relaxed transition-all duration-500 ease-in-out"
              :class="item.open ? 'max-h-96 opacity-100 pb-8' : 'max-h-0 opacity-0 pb-0'">
              {{ item.content }}
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Clean Minimal CTA -->
    <section class="py-32 px-4 bg-[#fcfcfc] text-center">
      <h2 class="font-garamond text-6xl text-novo-gray mb-8">Let's work <span class="text-novo-teal italic">together.</span></h2>
      <NuxtLink to="/contact" class="inline-flex items-center space-x-3 px-8 py-4 bg-novo-teal text-white rounded-full font-lexend font-medium tracking-wide hover:bg-novo-gray hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
        <span>Contact Novo Enviro</span>
        <Icon name="ph:paper-plane-tilt-fill" class="text-lg" />
      </NuxtLink>
    </section>
  </div>
</template>