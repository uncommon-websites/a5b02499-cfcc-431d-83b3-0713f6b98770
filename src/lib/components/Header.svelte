<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="fixed top-0 left-0 w-full z-50 bg-white/95 backdrop-blur-md transition-all duration-500 text-navy border-b border-gray-100">
  <div class="px-6 py-5 md:px-16 lg:px-24 md:py-6 flex justify-between items-center max-w-[1600px] mx-auto">
  <a href="/" class="flex items-center z-10">
    <img src="/logo.svg" alt="CG Operating Group" class="h-7 md:h-9" />
  </a>

  <nav class="hidden md:flex items-center gap-8 text-sm font-light">
    <a href="/needs" class="hover:text-teal transition-colors duration-300">Your Needs</a>
    <a href="/impact" class="hover:text-teal transition-colors duration-300">Impact</a>
    <a href="/firm" class="hover:text-teal transition-colors duration-300">Firm</a>
  </nav>

  <a href="/contact" class="px-5 py-2.5 border border-navy text-navy hover:bg-navy hover:text-white transition-all duration-300 z-10 text-sm font-normal tracking-wide">
    Contact
  </a>
  </div>
</header>
