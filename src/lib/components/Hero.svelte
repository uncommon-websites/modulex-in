<script>
  import Button from './Button.svelte';
</script>

<section class="relative h-screen min-h-[700px] flex items-center overflow-hidden">
  <!-- Background Image -->
  <div class="absolute inset-0 z-0">
    <img 
      src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?q=80&w=2070&auto=format&fit=crop" 
      alt="Modern Modular Building" 
      class="w-full h-full object-cover brightness-[0.6]"
    />
    <!-- Gradient Overlay -->
    <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-black/40"></div>
  </div>

  <div class="container mx-auto px-4 md:px-8 relative z-10 pt-20">
    <div class="max-w-4xl">
      <h1 class="text-5xl md:text-7xl font-medium text-white leading-tight mb-8">
        A New Era of Construction<br />
        Begins with Modular 2.0
      </h1>
      
      <div class="mb-12">
        <Button variant="primary">Book A Discovery Call</Button>
      </div>

      <div class="max-w-xl">
        <p class="text-white/90 text-lg leading-relaxed mb-8">
          Welcome to a new era of building manufacturing.<br/>
          High-precision steel modules arrive nearly complete,<br/>
          allowing you to earn revenue months sooner.
        </p>
        
        <!-- Slider Indicators -->
        <div class="flex gap-2">
          <div class="h-0.5 w-8 bg-white"></div>
          <div class="h-0.5 w-8 bg-white/30"></div>
        </div>
      </div>
    </div>
  </div>
</section>
