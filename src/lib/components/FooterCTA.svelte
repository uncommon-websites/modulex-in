<script>
  import Button from './Button.svelte';
</script>

<section class="relative h-[600px] flex items-center justify-center overflow-hidden">
  <div class="absolute inset-0 z-0">
    <img 
      src="https://images.unsplash.com/photo-1503387762-592deb58ef4e?q=80&w=2089&auto=format&fit=crop" 
      alt="Construction Crane" 
      class="w-full h-full object-cover"
    />
    <div class="absolute inset-0 bg-black/50"></div>
  </div>

  <div class="container mx-auto px-4 md:px-8 relative z-10 text-center">
    <h2 class="text-4xl md:text-6xl font-medium text-white mb-6">
      Unlock Your Project's Potential
    </h2>
    <p class="text-white/90 text-lg md:text-xl max-w-2xl mx-auto mb-10 leading-relaxed">
      Share your project details with a timeline, and we will return a customised programme, cost and ROI model within a week.
    </p>
    <Button variant="primary">Book A Discovery Call</Button>
  </div>
</section>
