<script>
  const sectors = [
    { name: "Hospitals And Clinics", active: true },
    { name: "Retail, Restaurants, QSRs, Clubs, Clubhouses", active: false },
    { name: "Educational Institutions", active: false },
    { name: "Residential (Apartments & Villas)", active: false },
    { name: "Hotels, Co-Living Spaces, Student Accommodations, Hostels", active: false },
    { name: "Corporate Offices", active: false },
  ];
</script>

<section class="py-24 bg-[#F9FAFB]">
  <div class="container mx-auto px-4 md:px-8">
    <div class="flex flex-col lg:flex-row justify-between items-start mb-16 gap-12">
      <div class="max-w-xl">
        <span class="text-[#E62E2D] font-medium text-sm tracking-widest uppercase mb-4 block">Use Cases</span>
        <h2 class="text-4xl md:text-5xl font-medium text-gray-900 leading-tight">
          Solving Sector<br />
          Challenges At Scale.
        </h2>
      </div>
      
      <div class="max-w-xl">
        <p class="text-gray-600 leading-relaxed">
          Modulex delivers modular pods and structures tailored to the needs of high-growth sectors. Our plug-and-play approach enables rapid deployment, consistent quality, & scalable design.
        </p>
      </div>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-start">
      <!-- Image -->
      <div class="relative h-[500px] w-full shadow-lg">
        <img 
          src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?q=80&w=2070&auto=format&fit=crop" 
          alt="Modern Hospital Building" 
          class="w-full h-full object-cover"
        />
        <!-- Optional overlay or badge could go here -->
      </div>

      <!-- List -->
      <div class="flex flex-col">
        {#each sectors as sector}
          <div class="group border-b border-gray-200 last:border-0">
            <button class="w-full py-6 flex items-center justify-between text-left transition-colors {sector.active ? 'text-[#E62E2D]' : 'text-gray-600 hover:text-gray-900'}">
              <span class="text-lg font-light {sector.active ? 'font-medium' : ''}">{sector.name}</span>
              <span class="ml-4 {sector.active ? 'text-[#E62E2D]' : 'text-gray-400 group-hover:text-gray-900'}">
                {#if sector.active}
                    <span class="text-sm font-medium mr-2">Know More</span>
                {/if}
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="inline-block">
                    <path d="M7 17L17 7" />
                    <path d="M7 7h10v10" />
                </svg>
              </span>
            </button>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
