<script>
  import Button from './Button.svelte';
  
  let isScrolled = false;
  
  function handleScroll() {
    isScrolled = window.scrollY > 50;
  }
</script>

<svelte:window on:scroll={handleScroll} />

<header class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {isScrolled ? 'bg-white/95 backdrop-blur-md shadow-sm py-4' : 'bg-transparent py-6'}">
  <div class="container mx-auto px-4 md:px-8 flex items-center justify-between">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-2 group">
        <!-- Placeholder for MODULEX logo -->
        <div class="flex flex-col">
            <span class="text-2xl font-bold tracking-[0.2em] uppercase {isScrolled ? 'text-gray-900' : 'text-white'}">Modulex</span>
            <div class="h-0.5 w-full bg-[#E62E2D] scale-x-100 origin-left transition-transform duration-300"></div>
        </div>
        <span class="text-[0.5rem] absolute -bottom-2 left-0 text-white opacity-0">Modern Method of Construction</span>
    </a>

    <!-- Navigation -->
    <nav class="hidden lg:flex items-center gap-10">
      {#each ['About', 'Why Modular', 'Technology'] as item}
        <a href="#{item.toLowerCase().replace(' ', '-')}" class="text-sm font-medium hover:text-[#E62E2D] transition-colors {isScrolled ? 'text-gray-700' : 'text-white'}">
          {item}
        </a>
      {/each}
      
      <div class="relative group">
        <button class="flex items-center gap-1 text-sm font-medium hover:text-[#E62E2D] transition-colors {isScrolled ? 'text-gray-700' : 'text-white'}">
          Solutions
          <svg width="10" height="10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M6 9l6 6 6-6"/>
          </svg>
        </button>
      </div>

      <a href="#investors" class="text-sm font-medium hover:text-[#E62E2D] transition-colors {isScrolled ? 'text-gray-700' : 'text-white'}">
        Investor Relations
      </a>

      <a href="#contact" class="flex items-center gap-2 text-sm font-medium hover:text-[#E62E2D] transition-colors {isScrolled ? 'text-gray-700' : 'text-white'}">
        Contact
        <span class="bg-white/20 rounded-full p-1">
            <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3">
            <path d="M7 17L17 7" />
            <path d="M7 7h10v10" />
            </svg>
        </span>
      </a>
    </nav>

    <!-- Mobile Menu Button (Hidden on Desktop) -->
    <button class="lg:hidden {isScrolled ? 'text-gray-900' : 'text-white'}">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <path d="M3 12h18M3 6h18M3 18h18"/>
      </svg>
    </button>
  </div>
</header>
