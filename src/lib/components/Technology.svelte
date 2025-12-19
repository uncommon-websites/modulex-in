<script>
  import Button from './Button.svelte';
</script>

<section class="py-24 bg-[#F9FAFB]">
  <div class="container mx-auto px-4 md:px-8">
    <div class="flex flex-col lg:flex-row justify-between items-start mb-16 gap-12">
      <div class="max-w-xl">
        <span class="text-[#E62E2D] font-medium text-sm tracking-widest uppercase mb-4 block">Technology</span>
        <h2 class="text-4xl md:text-5xl font-medium text-gray-900 leading-tight">
          Built With Precision.<br />
          Designed To Scale.
        </h2>
      </div>
      
      <div class="max-w-xl">
        <p class="text-gray-600 leading-relaxed mb-8">
          We use 3D modular construction and Light Gauge Steel Frame Technology. Each module is factory-built with structural framing, integrated MEP, and pre-finished interiors, ensuring minimal on-site disruption.
        </p>
        
        <!-- Sub Navigation -->
        <div class="flex items-center gap-8 text-sm text-gray-500 border-b border-gray-200 mb-8">
            <span class="text-gray-900 font-medium border-b-2 border-[#E62E2D] pb-4 px-1">Technology</span>
            <span class="hover:text-gray-900 cursor-pointer pb-4 px-1 transition-colors">Solutions</span>
            <span class="hover:text-gray-900 cursor-pointer pb-4 px-1 transition-colors">Use Cases</span>
            <span class="hover:text-gray-900 cursor-pointer pb-4 px-1 transition-colors">Sustainability</span>
        </div>

        <Button variant="primary">Our Technology</Button>
      </div>
    </div>

    <!-- Image Grid -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
      <!-- Left Image -->
      <div class="relative h-[450px] group overflow-hidden" 
           style="clip-path: polygon(0 0, 100% 0, 100% calc(100% - 40px), calc(100% - 40px) 100%, 0 100%);">
        <img 
          src="https://images.unsplash.com/photo-1541888946425-d81bb19240f5?q=80&w=2070&auto=format&fit=crop" 
          alt="Volumetric Module" 
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
        />
        <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/20 to-transparent"></div>
        <div class="absolute bottom-0 left-0 p-10 w-full pr-16">
          <h3 class="text-white text-3xl font-normal leading-tight">
            Volumetric Modules Built<br/>For Rapid Site Assembly
          </h3>
        </div>
      </div>

      <!-- Right Image -->
      <div class="relative h-[450px] group overflow-hidden">
        <img 
          src="https://images.unsplash.com/photo-1584622050111-993a426fbf0a?q=80&w=2070&auto=format&fit=crop" 
          alt="Factory Finished Bathroom" 
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
        />
        <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/20 to-transparent"></div>
        <div class="absolute bottom-0 left-0 p-10 w-full">
          <h3 class="text-white text-3xl font-normal leading-tight">
            Factory Finished Bathroom Pods<br/>Integrated Services And Interiors
          </h3>
        </div>
      </div>
    </div>
  </div>
</section>
