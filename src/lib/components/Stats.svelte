<script>
  const stats = [
    {
      value: "90%",
      label: "Built Offsite",
      icon: `<svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#E62E2D" stroke-width="1" stroke-linecap="square"><path d="M2 21h20"/><path d="M18 21V7l-6-4-6 4v14"/><path d="M12 3v4"/><path d="M12 21v-9"/><path d="M12 12l3-3"/><path d="M9 9l3 3"/></svg>` // Improved Crane/Building icon
    },
    {
      value: "30%",
      label: "Faster Output",
      icon: `<svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#E62E2D" stroke-width="1" stroke-linecap="square"><circle cx="12" cy="12" r="9"/><polyline points="12 6 12 12 16 14"/><path d="M12 2v2"/></svg>`
    },
    {
      value: "0",
      label: "Carbon Footprint",
      icon: `<svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#E62E2D" stroke-width="1" stroke-linecap="square"><path d="M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10z"/><path d="M12 6v6l4 2"/><circle cx="12" cy="12" r="3" stroke-dasharray="2 2"/></svg>` // Abstract gear/sun
    },
    {
      value: "40+",
      label: "Acre Factory Site",
      icon: `<svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#E62E2D" stroke-width="1" stroke-linecap="square"><path d="M3 21h18"/><path d="M5 21V7l8-4 8 4v14"/><rect x="8" y="11" width="8" height="6"/></svg>`
    }
  ];
</script>

<section class="py-20 bg-white">
  <div class="container mx-auto px-4 md:px-8">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
      {#each stats as stat}
        <div class="bg-white p-10 relative border border-gray-100 shadow-sm group hover:shadow-md transition-all duration-300 min-h-[280px] flex flex-col justify-between" 
             style="clip-path: polygon(0 0, 100% 0, 100% calc(100% - 30px), calc(100% - 30px) 100%, 0 100%);">
             <!-- We need a pseudo-element for the border if we use clip-path, but clip-path clips the border too. 
                  Instead, let's use a filter drop-shadow to show the shape, or just rely on the background difference if the section was gray.
                  Since the section is white, and cards are white, we need a border. 
                  However, standard border is clipped. 
                  Let's try a different approach: SVG background or just a subtle shadow that respects the clip?
                  Actually, drop-shadow works on clipped elements.
             -->
             
          <div class="mb-6">
            {@html stat.icon}
          </div>
          <div>
            <h3 class="text-6xl font-light text-gray-900 mb-4 tracking-tight">{stat.value}</h3>
            <p class="text-gray-500 text-sm uppercase tracking-widest font-medium">{stat.label}</p>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
    /* Add a subtle drop shadow that follows the clip-path shape */
    div[style*="clip-path"] {
        filter: drop-shadow(0 4px 6px rgba(0, 0, 0, 0.05));
    }
</style>
