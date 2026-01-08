<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import { page } from '$app/stores';
  import { onMount } from 'svelte';

  let formData = {
    name: '',
    email: '',
    company: '',
    need: '',
    message: ''
  };

  let isSubmitting = false;
  let submitted = false;

  onMount(() => {
    const needParam = $page.url.searchParams.get('need');
    if (needParam && ['manufacturing', 'distribution', 'both', 'other'].includes(needParam)) {
      formData.need = needParam;
    }
  });

  async function handleSubmit() {
    isSubmitting = true;
    await new Promise(resolve => setTimeout(resolve, 1000));
    submitted = true;
    isSubmitting = false;
  }
</script>

<Header />

<main class="pt-20 md:pt-0 font-sans text-navy">

  <!-- Split Screen Layout -->
  <div class="min-h-screen flex flex-col lg:flex-row">

    <!-- Left Side - Image & Text -->
    <div class="lg:w-1/2 lg:fixed lg:left-0 lg:top-0 lg:h-screen relative">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <img src="/port.webp" alt="Global Operations" class="w-full h-full object-cover" />
        <div class="absolute inset-0 bg-gradient-to-t from-navy/90 via-navy/50 to-navy/30"></div>
      </div>

      <!-- Content Overlay -->
      <div class="relative z-10 h-full flex flex-col justify-end p-8 md:p-12 lg:p-16 xl:p-20 min-h-[50vh] lg:min-h-screen">
        <div class="max-w-xl">
          <p class="text-white/60 text-xs tracking-widest uppercase font-medium mb-6 animate-fade-in">Contact</p>
          <h1 class="text-3xl md:text-4xl lg:text-5xl xl:text-6xl font-light text-white leading-[1.1] tracking-tight mb-6 animate-fade-in-up">
            Unlock the potential of your supply chain.
          </h1>
          <p class="text-lg md:text-xl text-white/70 font-light leading-relaxed animate-fade-in-up-delay">
            What we hear from clients: <span class="text-white">we wish we had this in place before.</span>
          </p>
        </div>
      </div>
    </div>

    <!-- Right Side - Form -->
    <div class="lg:w-1/2 lg:ml-[50%] bg-white">
      <div class="min-h-screen flex items-center">
        <div class="w-full px-8 md:px-12 lg:px-16 xl:px-24 py-16 lg:py-24">
          <div class="max-w-lg mx-auto lg:mx-0">

            {#if submitted}
              <div class="animate-fade-in">
                <div class="w-16 h-16 rounded-full bg-teal/10 flex items-center justify-center mb-8">
                  <svg class="w-8 h-8 text-teal" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 13l4 4L19 7" />
                  </svg>
                </div>
                <h2 class="text-3xl md:text-4xl font-light text-navy mb-4 tracking-tight">Message sent.</h2>
                <p class="text-gray-500 font-light text-lg leading-relaxed">
                  We'll be in touch within 24 hours to discuss how we can help.
                </p>
                <a href="/" class="inline-block mt-8 text-navy font-medium hover:text-teal transition-colors duration-150">
                  Back to Home
                </a>
              </div>
            {:else}
              <div class="mb-12">
                <h2 class="text-2xl md:text-3xl font-light text-navy tracking-tight mb-4">Start a conversation</h2>
                <p class="text-gray-500 font-light leading-relaxed">
                  Tell us about your challenge. We'll tell you if we're the right fit. No sales pitch. No obligation.
                </p>
              </div>

              <form on:submit|preventDefault={handleSubmit} class="space-y-6">
                <!-- Name & Email Row -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                  <div class="group">
                    <label for="name" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3 group-focus-within:text-navy transition-colors duration-150">Name</label>
                    <input
                      type="text"
                      id="name"
                      bind:value={formData.name}
                      required
                      class="w-full px-0 py-3 bg-transparent border-0 border-b-2 border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy transition-all duration-300 placeholder:text-gray-300"
                      placeholder="Your name"
                    />
                  </div>
                  <div class="group">
                    <label for="email" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3 group-focus-within:text-navy transition-colors duration-150">Email</label>
                    <input
                      type="email"
                      id="email"
                      bind:value={formData.email}
                      required
                      class="w-full px-0 py-3 bg-transparent border-0 border-b-2 border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy transition-all duration-300 placeholder:text-gray-300"
                      placeholder="you@company.com"
                    />
                  </div>
                </div>

                <!-- Company & Need Row -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                  <div class="group">
                    <label for="company" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3 group-focus-within:text-navy transition-colors duration-150">Company</label>
                    <input
                      type="text"
                      id="company"
                      bind:value={formData.company}
                      required
                      class="w-full px-0 py-3 bg-transparent border-0 border-b-2 border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy transition-all duration-300 placeholder:text-gray-300"
                      placeholder="Company name"
                    />
                  </div>
                  <div class="group">
                    <label for="need" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3 group-focus-within:text-navy transition-colors duration-150">Primary Need</label>
                    <div class="relative">
                      <select
                        id="need"
                        bind:value={formData.need}
                        required
                        class="w-full px-0 py-3 bg-transparent border-0 border-b-2 border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy transition-all duration-300 cursor-pointer appearance-none"
                      >
                        <option value="" disabled class="text-gray-400">Select one</option>
                        <option value="manufacturing">Manufacturing</option>
                        <option value="distribution">Distribution</option>
                        <option value="both">Both</option>
                        <option value="other">Other</option>
                      </select>
                      <div class="absolute right-0 top-1/2 -translate-y-1/2 pointer-events-none">
                        <svg class="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M19 9l-7 7-7-7" />
                        </svg>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- Message -->
                <div class="group">
                  <label for="message" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3 group-focus-within:text-navy transition-colors duration-150">Your Challenge</label>
                  <textarea
                    id="message"
                    bind:value={formData.message}
                    required
                    rows="4"
                    minlength="20"
                    class="w-full px-0 py-3 bg-transparent border-0 border-b-2 border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy transition-all duration-300 placeholder:text-gray-300 resize-none"
                    placeholder="What challenges are you facing with manufacturing or distribution?"
                  ></textarea>
                </div>

                <!-- Submit -->
                <div class="pt-6">
                  <button
                    type="submit"
                    disabled={isSubmitting}
                    class="group relative px-10 py-4 bg-navy text-white text-sm font-medium tracking-wide overflow-hidden transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed hover:bg-navy-600"
                  >
                    <span class="relative z-10">{isSubmitting ? 'Sending...' : 'Send Message'}</span>
                  </button>
                </div>
              </form>

              <!-- Trust Indicator -->
              <div class="mt-16 pt-8 border-t border-gray-100">
                <p class="text-xs text-gray-400 font-light">
                  Your information is kept confidential. We respond to all inquiries within 24 hours.
                </p>
              </div>
            {/if}

          </div>
        </div>
      </div>
    </div>

  </div>

  <!-- Footer - Only visible on mobile or when scrolled past form -->
  <footer class="bg-navy text-white lg:relative">
    <div class="py-16 md:py-20">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
        <div class="grid grid-cols-2 md:grid-cols-5 gap-10 md:gap-8">
          <div class="col-span-2 md:col-span-2">
            <img src="/logo-footer.svg" alt="CG Operating Group" class="h-10 brightness-0 invert" />
          </div>

          <div>
            <p class="text-xs tracking-wider text-white/40 mb-5">Navigate</p>
            <nav class="flex flex-col gap-2.5">
              <a href="/needs" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Your Needs</a>
              <a href="/impact" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Our Impact</a>
              <a href="/firm" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Our Firm</a>
            </nav>
          </div>

          <div>
            <p class="text-xs tracking-wider text-white/40 mb-5">Services</p>
            <nav class="flex flex-col gap-2.5">
              <a href="/needs?tab=manufacturing" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Manufacturing</a>
              <a href="/needs?tab=distribution" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Distribution</a>
            </nav>
          </div>

          <div>
            <p class="text-xs tracking-wider text-white/40 mb-5">Connect</p>
            <nav class="flex flex-col gap-2.5">
              <a href="/contact" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Contact</a>
              <a href="https://x.com" class="text-sm text-white/70 hover:text-white transition-colors duration-150">X</a>
              <a href="https://linkedin.com" class="text-sm text-white/70 hover:text-white transition-colors duration-150">LinkedIn</a>
            </nav>
          </div>
        </div>
      </div>
    </div>

    <div class="py-5 border-t border-white/10">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
        <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-3">
          <p class="text-xs text-white/40">© 2025 CG Operating Group</p>
          <div class="flex items-center gap-4">
            <a href="/privacy" class="text-xs text-white/40 hover:text-white/70 transition-colors duration-150">Privacy Policy</a>
            <a href="/terms" class="text-xs text-white/40 hover:text-white/70 transition-colors duration-150">Terms of Service</a>
          </div>
        </div>
      </div>
    </div>
  </footer>

</main>

<style>
  @keyframes fade-in {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  @keyframes fade-in-up {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .animate-fade-in {
    animation: fade-in 0.6s ease-out forwards;
  }

  .animate-fade-in-up {
    animation: fade-in-up 0.8s ease-out forwards;
  }

  .animate-fade-in-up-delay {
    animation: fade-in-up 0.8s ease-out 0.2s forwards;
    opacity: 0;
  }
</style>
