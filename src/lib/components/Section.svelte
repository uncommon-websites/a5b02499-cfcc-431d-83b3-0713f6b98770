<script lang="ts">
  export let label: string = "";
  export let link: string | undefined = undefined;
  export let linkText: string = "";
</script>

<section class="flex flex-col md:flex-row w-full py-20 md:py-32 border-t border-transparent">
  <div class="w-full md:w-1/4 mb-12 md:mb-0 pr-8">
    <h3 class="text-xs tracking-wider uppercase text-gray-400 font-medium">{label}</h3>
  </div>
  <div class="w-full md:w-3/4">
    {#if link}
      <div class="flex justify-end mb-12 -mt-12 md:mt-0">
        <a href={link} class="text-base text-gray-400 hover:text-teal transition-colors duration-300 flex items-center gap-2 group font-light">
          {linkText}
          <span class="group-hover:translate-x-1 transition-transform duration-300">→</span>
        </a>
      </div>
    {/if}
    <slot />
  </div>
</section>
