<script lang="ts">
  export let href = "#";
  export let variant: "primary" | "outline" | "white" = "primary";
  export let className = "";
</script>

<a
  {href}
  class="inline-flex items-center justify-center px-6 py-3 text-sm font-medium transition-colors duration-200 {className} {variant === 'primary' ? 'bg-[#E62E2D] text-white hover:bg-[#c42524]' : variant === 'white' ? 'bg-white text-[#E62E2D] hover:bg-gray-100' : 'border border-white text-white hover:bg-white/10'}"
>
  <slot />
  <span class="ml-2 bg-white/20 p-1">
    <svg width="10" height="10" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="square" stroke-linejoin="miter">
      <path d="M7 17L17 7" />
      <path d="M7 7h10v10" />
    </svg>
  </span>
</a>
