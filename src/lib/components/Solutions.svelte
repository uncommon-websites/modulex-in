<script>
  import Button from './Button.svelte';
</script>

<section class="py-24 bg-white">
  <div class="container mx-auto px-4 md:px-8">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
      
      <!-- Content -->
      <div>
        <span class="text-[#E62E2D] font-medium text-sm tracking-widest uppercase mb-4 block">Solutions</span>
        <h2 class="text-4xl md:text-5xl font-medium text-gray-900 leading-tight mb-6">
          From Bathroom<br/>
          Pods To Kitchen<br/>
          Units, All<br/>
          Factory-Built.
        </h2>
        
        <p class="text-gray-600 leading-relaxed mb-8 max-w-md">
          Whether it's a standalone pod or a full volumetric structure, our solutions are based on pre-engineered steel modules that are durable, fire-safe & compliant with global standards.
        </p>

        <div class="mb-12">
            <Button variant="primary">Our Solutions</Button>
        </div>

        <!-- Navigation Arrows -->
        <div class="flex gap-4">
          <button class="w-12 h-12 border border-gray-200 flex items-center justify-center hover:border-[#E62E2D] hover:text-[#E62E2D] transition-colors">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M19 12H5M12 19l-7-7 7-7"/>
            </svg>
          </button>
          <button class="w-12 h-12 border border-gray-200 flex items-center justify-center hover:border-[#E62E2D] hover:text-[#E62E2D] transition-colors">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M5 12h14M12 5l7 7-7 7"/>
            </svg>
          </button>
        </div>
      </div>

      <!-- Image -->
      <div class="relative h-[600px] w-full" style="clip-path: polygon(0 0, 100% 0, 100% calc(100% - 60px), calc(100% - 60px) 100%, 0 100%);">
        <img 
          src="https://images.unsplash.com/photo-1556911220-bff31c812dba?q=80&w=2068&auto=format&fit=crop" 
          alt="Kitchen Pod" 
          class="w-full h-full object-cover"
        />
        <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent"></div>
        <div class="absolute bottom-0 left-0 p-8 w-full">
          <h3 class="text-white text-xl font-medium">
            Utility Pods - Kitchen Pods
          </h3>
        </div>
      </div>

    </div>
  </div>
</section>
