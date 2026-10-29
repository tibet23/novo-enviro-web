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
    <section class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-12 items-center">
      <!-- Left Column with Smooth Fade-in & Lift -->
      <div 
        class="transition-all duration-1000 ease-out"
        :class="isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'">
        <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-6">Certified Plastic Credits</p>
        <h1 class="font-garamond text-5xl md:text-6xl text-novo-gray mb-2">From <span class="italic text-novo-teal">Waste</span></h1>
        <h2 class="font-garamond italic text-5xl md:text-6xl text-novo-gray mb-8">to <span class="text-novo-teal">Worth.</span></h2>
        
        <!-- Expanding Teal Line -->
        <div 
          class="h-[2px] bg-novo-teal mb-8 transition-all duration-1000 delay-300 ease-out"
          :class="isLoaded ? 'w-12 opacity-100' : 'w-0 opacity-0'">
        </div>

        <div class="font-lexend font-light text-novo-gray text-sm leading-relaxed space-y-4 max-w-lg">
          <p>
            Novo Enviro is a <strong class="font-semibold text-novo-gray">plastic credit project developer and consultancy</strong>. We help plastic recycling companies and plastic waste aggregators generate certified plastic credits through internationally recognised independent standard organisations. From additionality assessment to credit issuance — end to end.
          </p>
          <p>
            Our mission: helping the industry collectively generate <strong class="font-semibold text-novo-gray">100,000,000 kilograms</strong> of verified plastic credits.
          </p>
        </div>
      </div>
      
      <!-- Right Column with Staggered Fade-in & Floating Hover on Stat -->
      <div 
        class="text-center md:text-right transition-all duration-1000 delay-200 ease-out"
        :class="isLoaded ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'">
        <p class="font-lexend font-bold italic text-novo-gray text-xl md:text-2xl mb-12">
          "Turn your recycling operation into <span class="text-novo-teal">plastic credits</span>"
        </p>
        
        <div class="inline-block text-left transition-transform duration-300 hover:-translate-y-1">
          <p class="font-lexend font-medium text-novo-gray underline mb-4">Initial Target</p>
          <p class="font-lexend font-bold text-6xl text-novo-gray mb-1">100<span class="text-novo-teal">M</span></p>
          <p class="font-lexend font-bold text-sm tracking-widest text-novo-gray uppercase">Kilograms</p>
          <p class="font-lexend font-light text-xs text-novo-gray uppercase">Of Certified Plastic Credits</p>
        </div>
      </div>
    </section>

    <!-- Plastic Credit Quality Section -->
    <section class="max-w-5xl mx-auto px-4 py-8 border-t border-gray-200">
      <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-4">Plastic Credit Quality</p>
      <h2 class="font-garamond text-4xl md:text-5xl text-novo-gray leading-tight">Four criteria.</h2>
      <h3 class="font-garamond italic text-4xl md:text-5xl text-novo-teal mb-6">No exceptions.</h3>
      
      <p class="font-lexend font-light text-novo-gray text-sm md:text-base mb-12 max-w-3xl">
        Every plastic credit project we certify must satisfy all four quality criteria. These are the standards that protect buyers, communities, and the long-term integrity of the plastic credit market.
      </p>

      <div class="grid md:grid-cols-4 gap-6 font-lexend text-novo-gray">
        <div>
          <p class="text-novo-teal text-xs font-medium mb-2">01</p>
          <h4 class="font-medium text-sm mb-4">Sound Environmental Process</h4>
          <p class="text-xs font-light leading-relaxed">Plastic must be collected and processed through genuinely sound environmental practices. Displacement of harm to another location is not accepted. We assess the full downstream processing chain to confirm the plastic is being recovered in a manner that meets applicable environmental regulations.</p>
        </div>
        <div>
          <p class="text-novo-teal text-xs font-medium mb-2">02</p>
          <h4 class="font-medium text-sm mb-4">Additionality and Ownership</h4>
          <p class="text-xs font-light leading-relaxed">Collection activity is additional — it would not have occurred without the credit incentive. Ownership is clearly defined and non-duplicative: only one party may hold and claim the credit for each kilogram of plastic recovered. No shared claims, no contested attribution.</p>
        </div>
        <div>
          <p class="text-novo-teal text-xs font-medium mb-2">03</p>
          <h4 class="font-medium text-sm mb-4">Safeguard Systems</h4>
          <p class="text-xs font-light leading-relaxed">Robust social and environmental safeguards are in place. Workers are protected. Community wellbeing is not compromised by project activity. Safeguard protocols are developed at project design stage and monitored at each verification cycle.</p>
        </div>
        <div>
          <p class="text-novo-teal text-xs font-medium mb-2">04</p>
          <h4 class="font-medium text-sm mb-4">Traceability and Transparency</h4>
          <p class="text-xs font-light leading-relaxed">Every kilogram of plastic is traceable from collection to certified credit. Full chain-of-custody transparency is required throughout. Nothing is obscured, estimated without basis, or asserted without documentation.</p>
        </div>
      </div>
    </section>

    <!-- Project Portfolio Intro Section -->
    <section class="max-w-5xl mx-auto px-4 py-8 border-t border-gray-200">
      <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-6">Project Portfolio</p>
      <div class="font-garamond text-4xl md:text-5xl text-novo-gray leading-tight mb-8">
        <p>Proof, <span class="italic text-novo-teal">on the registry.</span></p>
      </div>

      <div class="space-y-6 font-lexend text-novo-gray text-sm md:text-base leading-relaxed font-light">
        <p>
          Novo Enviro develops high quality certified plastic credit projects end to end — from additionality assessment to credit issuance. Every project we bring to registry is independently verified by a third-party body and recorded on a public registry, ensuring full traceability and preventing double-counting.
        </p>
        <p class="font-semibold">
          The portfolio below is where that process becomes proof: real projects, real credits, each one ready for retirement.
        </p>
      </div>
    </section>
    
    <!-- Custom Project Portfolio Widget Block -->
    <section class="max-w-5xl mx-auto px-4 mb-16">
      <div class="border border-novo-teal bg-[#fcfcfc]">
        
        <!-- Header -->
        <div class="bg-novo-teal px-6 py-3 flex justify-between items-center text-xs tracking-widest text-white font-mono uppercase">
          <span class="bg-[#fcfcfc] text-novo-teal px-3 py-1 font-medium">★ Flagship Project</span>
          <span class="font-bold">1st PPRS-Registered Project in Türkiye</span>
        </div>
        
        <!-- Title Block -->
        <div class="p-6 border-b border-novo-teal">
          <p class="font-lexend text-xs tracking-[0.2em] text-novo-teal uppercase mb-3">Düzce, Türkiye</p>
          <h3 class="font-garamond text-2xl text-novo-gray max-w-2xl">Community and Institutional Collection of HDPE, PET, and Nylon for Mechanical Recycling</h3>
        </div>
        
        <!-- Stats Grid -->
        <div class="grid grid-cols-2 md:grid-cols-4 border-b border-novo-teal text-novo-gray">
          <div class="p-5 border-r border-b md:border-b-0 border-novo-teal">
            <p class="font-garamond text-2xl font-bold text-novo-teal mb-1">500,000 <span class="text-sm font-normal">kg</span></p>
            <p class="font-lexend text-[10px] tracking-widest uppercase">Annual Plastic Collection Capacity</p>
          </div>
          <div class="p-5 border-r border-b md:border-b-0 border-novo-teal">
            <p class="font-garamond text-2xl font-bold text-novo-teal mb-1">3</p>
            <p class="font-lexend text-[10px] tracking-widest uppercase">Polymers<br>HDPE · PET · Nylon</p>
          </div>
          <div class="p-5 border-r border-novo-teal">
            <p class="font-garamond text-2xl font-bold text-novo-teal mb-1">6</p>
            <p class="font-lexend text-[10px] tracking-widest uppercase">SDGs Achieved</p>
          </div>
          <div class="p-5">
            <p class="font-garamond text-xl font-bold text-novo-teal mb-1">Mechanical recycling</p>
            <p class="font-lexend text-[10px] tracking-widest uppercase">Treatment Method</p>
          </div>
        </div>
        
        <!-- Key/Value Grid -->
        <div class="grid md:grid-cols-2 text-novo-gray">
          <div class="p-4 border-r border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Standard</p>
            <p class="font-lexend text-sm">Plastic Pollution Reduction Standard</p>
          </div>
          <div class="p-4 border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Registry</p>
            <p class="font-lexend text-sm">The PPRS Registry</p>
          </div>
          <div class="p-4 border-r border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Independent Auditor</p>
            <p class="font-lexend text-sm">Accredited Third-Party VVB</p>
          </div>
          <div class="p-4 border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Project Partner</p>
            <p class="font-lexend text-sm">Sevel Geri Dönüşüm</p>
          </div>
          <div class="p-4 border-r border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Location</p>
            <p class="font-lexend text-sm">Düzce, Türkiye · a coastal province on the Black Sea</p>
          </div>
          <div class="p-4 border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Polymers Recovered</p>
            <p class="font-lexend text-sm">HDPE · PET · Nylon</p>
          </div>
          <div class="p-4 border-r border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Activity</p>
            <p class="font-lexend text-sm">Collection · Aggregation · Mechanical Recycling</p>
          </div>
          <div class="p-4 border-b border-novo-teal">
            <p class="font-lexend text-[10px] tracking-[0.14em] uppercase text-novo-teal mb-1">Annual Plastic Credit Capacity</p>
            <p class="font-lexend text-sm">500</p>
          </div>
        </div>
        
        <!-- Project Description -->
        <div class="p-6 border-b border-novo-teal font-lexend font-light text-sm text-novo-gray space-y-4">
          <p class="text-[10px] tracking-[0.2em] text-novo-teal uppercase mb-2">Project Description</p>
          <p><strong class="font-bold text-novo-gray">This is the first PPRS-registered plastic credit project in Türkiye</strong>, and one of the country's first plastic credit projects. It creates a sustainable and effective system for collecting, aggregating, and recycling post-consumer HDPE, PET, and Nylon waste in Düzce, Türkiye — complementing existing waste management infrastructure by strengthening dedicated plastic separation and recovery across the region.</p>
          <p>Düzce is a coastal province in northwestern Türkiye, with a dedicated coastline on the Black Sea and a region exceptionally rich in streams, creeks, and groundwater reserves. Local waterways feed the Büyük Melen River, the region's principal watercourse, on its way to the Black Sea. As plastic consumption grows across the city, expanding dedicated plastic collection capacity has become an environmental priority. Plastics are intercepted before they can fragment into microplastics that reach local waterways, aquifers, and the Black Sea basin — and before they reach open dumps.</p>
          <p>By building out plastic collection and aggregation services across the region, the project organizes and trains waste pickers recovering post-consumer plastics from households, restaurants, retail stores, farmers' markets, public events, workplaces, construction sites, and municipal collection points. Collected materials are sorted, baled to commercial specification, and transferred to mechanical recyclers — reducing dependence on virgin polymer production and avoiding associated GHG emissions through resource recovery.</p>
          <p>Beyond its environmental impact, the project drives meaningful social change. It increases income for informal waste sector workers and participating community members, expands local employment opportunities, and actively improves conditions and dignity for waste pickers. With particular emphasis on creating opportunities for women and strengthening community participation in plastic separation, the project contributes to broader local and social development.</p>
          
          <div class="flex items-center gap-4 mt-6 p-4 border border-novo-teal">
            <span class="font-garamond text-2xl font-bold text-novo-teal whitespace-nowrap">≈ 15M</span>
            <span class="text-xs"><strong class="font-bold text-novo-gray">500 ml empty HDPE plastic bottles, by weight.</strong> The 500,000 kilograms of annual plastic collection capacity under this project is equivalent to roughly 15 million plastic bottles diverted from the environment and returned to productive use.</span>
          </div>
        </div>
        
        <!-- SDGs -->
        <div class="p-6 border-b border-novo-teal">
          <p class="font-lexend text-[10px] tracking-[0.2em] text-novo-teal uppercase mb-4">UN Sustainable Development Goals Achieved</p>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-3">
            <div class="border border-novo-teal border-t-2 p-4 bg-white">
              <p class="font-garamond text-lg font-bold text-novo-teal mb-1">SDG 1</p>
              <p class="font-lexend text-sm font-medium text-novo-gray mb-1">No Poverty</p>
              <p class="font-lexend text-xs font-light text-novo-gray">Provides income and employment opportunities to informal waste workers and marginalized groups, reducing poverty levels.</p>
            </div>
            <div class="border border-novo-teal border-t-2 p-4 bg-white">
              <p class="font-garamond text-lg font-bold text-novo-teal mb-1">SDG 6</p>
              <p class="font-lexend text-sm font-medium text-novo-gray mb-1">Clean Water and Sanitation</p>
              <p class="font-lexend text-xs font-light text-novo-gray">Prevents plastic waste from entering waterways, protecting water bodies from pollution and improving sanitation conditions.</p>
            </div>
            <div class="border border-novo-teal border-t-2 p-4 bg-white">
              <p class="font-garamond text-lg font-bold text-novo-teal mb-1">SDG 8</p>
              <p class="font-lexend text-sm font-medium text-novo-gray mb-1">Decent Work and Economic Growth</p>
              <p class="font-lexend text-xs font-light text-novo-gray">Creates dignified green jobs in waste management and recycling, often benefiting low-income and underserved communities.</p>
            </div>
            <div class="border border-novo-teal border-t-2 p-4 bg-white">
              <p class="font-garamond text-lg font-bold text-novo-teal mb-1">SDG 9</p>
              <p class="font-lexend text-sm font-medium text-novo-gray mb-1">Industry, Innovation, and Infrastructure</p>
              <p class="font-lexend text-xs font-light text-novo-gray">Encourages the development of circular economy infrastructure, such as Material Recovery Facilities (MRFs) and recycling units.</p>
            </div>
            <div class="border border-novo-teal border-t-2 p-4 bg-white">
              <p class="font-garamond text-lg font-bold text-novo-teal mb-1">SDG 11</p>
              <p class="font-lexend text-sm font-medium text-novo-gray mb-1">Sustainable Cities and Communities</p>
              <p class="font-lexend text-xs font-light text-novo-gray">Contributes to cleaner urban environments and better municipal waste management systems.</p>
            </div>
            <div class="border border-novo-teal border-t-2 p-4 bg-white">
              <p class="font-garamond text-lg font-bold text-novo-teal mb-1">SDG 13</p>
              <p class="font-lexend text-sm font-medium text-novo-gray mb-1">Climate Action</p>
              <p class="font-lexend text-xs font-light text-novo-gray">Avoids greenhouse gas emissions by reducing landfill use and replacing virgin plastic production with recycled inputs.</p>
            </div>
          </div>
        </div>
        
        <!-- Impact & Co-Benefits -->
        <div class="p-6 border-b border-novo-teal">
          <p class="font-lexend text-[10px] tracking-[0.2em] text-novo-teal uppercase mb-4">Impact & Co-Benefits</p>
          <div class="grid md:grid-cols-2 gap-8 font-lexend font-light text-sm text-novo-gray">
            <div>
              <p class="text-[10px] tracking-[0.16em] uppercase text-novo-teal mb-2">Environmental</p>
              <ul class="space-y-3">
                <li class="border-b border-novo-teal pb-2 relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Diverts plastic waste from nature and sea</li>
                <li class="border-b border-novo-teal pb-2 relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> GHG emissions reduced through resource recovery</li>
                <li class="relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Protects the Black Sea basin from microplastic contamination</li>
              </ul>
            </div>
            <div>
              <p class="text-[10px] tracking-[0.16em] uppercase text-novo-teal mb-2">Social</p>
              <ul class="space-y-3">
                <li class="border-b border-novo-teal pb-2 relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Increased income for the informal waste sector</li>
                <li class="border-b border-novo-teal pb-2 relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Expanded opportunities for women</li>
                <li class="border-b border-novo-teal pb-2 relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Higher community participation in plastic separation</li>
                <li class="border-b border-novo-teal pb-2 relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Improved dignity and conditions for waste pickers</li>
                <li class="relative pl-4"><span class="absolute left-0 text-novo-teal">—</span> Local employment and community development</li>
              </ul>
            </div>
          </div>
        </div>
        
        <!-- Why PPRS -->
        <div class="p-6">
          <p class="font-lexend text-[10px] tracking-[0.2em] text-novo-teal uppercase mb-3">Why PPRS</p>
          <h3 class="font-garamond text-xl text-novo-gray mb-3">The standard behind <span class="italic text-novo-teal">the credit.</span></h3>
          <p class="font-lexend font-light text-sm text-novo-gray mb-5 max-w-3xl">The Plastic Pollution Reduction Standard (PPRS), created by PCX Solutions, sets a rigorous framework for registering post-consumer plastic recovery projects and issuing plastic credits. It spans the full lifecycle — from collection through processing — enforces strict environmental and social safeguards, and requires end-to-end, third-party impact verification. <strong class="font-bold text-novo-gray">Registration under PPRS is what makes a credit traceable, accountable, and trusted by institutional buyers.</strong></p>
          
          <div class="grid md:grid-cols-3 gap-6 font-lexend text-novo-gray border-t border-novo-teal pt-4">
            <div>
              <p class="font-medium text-sm mb-1">Comprehensive scope</p>
              <p class="font-light text-xs">Covers both collection — ocean, ocean-bound, landfill diversion — and processing through recycling, upcycling, and co-processing.</p>
            </div>
            <div>
              <p class="font-medium text-sm mb-1">Strict safeguards</p>
              <p class="font-light text-xs">Built-in environmental and social safeguards protect ecosystems, workers, and the communities where recovery takes place.</p>
            </div>
            <div>
              <p class="font-medium text-sm mb-1">End-to-end verification</p>
              <p class="font-light text-xs">A robust, independent impact-verification process ensures full accountability and transparency from collection to issuance.</p>
            </div>
          </div>
        </div>
        
        <!-- Card CTA Footer -->
        <div class="bg-novo-teal p-6 flex flex-col md:flex-row justify-between items-center gap-4">
          <div>
            <p class="font-garamond text-xl text-white mb-1">Retire verified, high-quality plastic credits from our flagship project.</p>
            <p class="font-mono text-xs text-white tracking-wider">PPRS certified · Independently verified</p>
          </div>
          <NuxtLink 
            to="/contact" 
            class="bg-white text-novo-teal font-lexend font-semibold text-xs tracking-wider uppercase px-7 py-3.5 rounded-full whitespace-nowrap hover:bg-gray-100 transition-colors shadow-sm">
            Talk to Novo Enviro
          </NuxtLink>
        </div>
      </div>
    </section>

    <!-- In Development Bottom Section -->
    <section class="max-w-4xl mx-auto px-4 text-center border-t border-gray-200 pt-16">
      <p class="text-novo-teal text-xs tracking-[0.25em] uppercase font-medium mb-6">In Development</p>
      <h2 class="font-garamond text-4xl md:text-5xl text-novo-gray mb-8">Toward <span class="italic text-novo-teal">100 million kilograms.</span></h2>
      
      <p class="font-lexend font-light text-novo-gray text-sm md:text-base mb-12 max-w-3xl mx-auto leading-relaxed">
        We're continuously originating new projects with plastic collection and recycling partners across the region to get there — and we're always looking for the next operation to certify. <strong class="font-semibold text-novo-gray">Ready to earn <span class="text-novo-teal">plastic credits?</span></strong> If you collect, sort or process post-consumer plastic, let's talk.
      </p>
      
      <div class="flex justify-center pt-8 pb-12">
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