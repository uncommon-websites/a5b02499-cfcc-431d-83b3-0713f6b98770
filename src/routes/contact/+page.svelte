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
    // Simulate form submission
    await new Promise(resolve => setTimeout(resolve, 1000));
    submitted = true;
    isSubmitting = false;
  }
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero -->
  <div class="py-20 md:py-32">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16">
        <div class="lg:col-span-3">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium">Contact</p>
        </div>
        <div class="lg:col-span-9">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-navy leading-[1.1] max-w-3xl">
            Let's discuss how we can support your growth.
          </h1>
          <p class="mt-6 text-xl md:text-2xl text-gray-400 font-light max-w-2xl leading-relaxed">
            The thing we hear most often: "We wish we'd called you sooner."
          </p>
        </div>
      </div>
    </div>
  </div>

  <!-- Form Section -->
  <div class="py-16 md:py-24 border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16">

        <!-- Left Column - Info -->
        <div class="lg:col-span-4">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-8">Get in Touch</p>

          <div class="space-y-8">
            <div>
              <p class="text-sm tracking-widest uppercase text-navy font-medium mb-2">Email</p>
              <a href="mailto:contact@cgoperatinggroup.com" class="text-lg text-gray-500 font-light hover:text-teal transition-colors duration-150">
                contact@cgoperatinggroup.com
              </a>
            </div>

            <div>
              <p class="text-sm tracking-widest uppercase text-navy font-medium mb-2">LinkedIn</p>
              <a href="https://linkedin.com" class="text-lg text-gray-500 font-light hover:text-teal transition-colors duration-150">
                CG Operating Group
              </a>
            </div>

            <div class="pt-8 border-t border-gray-100">
              <p class="text-gray-500 font-light leading-relaxed">
                Tell us about your challenge. We'll tell you if we're the right fit. No sales pitch. No obligation.
              </p>
            </div>
          </div>
        </div>

        <!-- Right Column - Form -->
        <div class="lg:col-span-8">
          {#if submitted}
            <div class="bg-gray-50 p-12 md:p-16">
              <h2 class="text-2xl md:text-3xl font-light text-navy mb-4 tracking-tight">Message sent.</h2>
              <p class="text-gray-500 font-light text-lg">We'll be in touch within 24 hours.</p>
            </div>
          {:else}
            <form on:submit|preventDefault={handleSubmit} class="space-y-8">
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div>
                  <label for="name" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3">Name</label>
                  <input
                    type="text"
                    id="name"
                    bind:value={formData.name}
                    required
                    class="w-full px-4 py-4 bg-gray-50 border border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy focus:bg-white transition-all duration-150 placeholder:text-gray-400"
                    placeholder="Your name"
                  />
                </div>
                <div>
                  <label for="email" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3">Email</label>
                  <input
                    type="email"
                    id="email"
                    bind:value={formData.email}
                    required
                    class="w-full px-4 py-4 bg-gray-50 border border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy focus:bg-white transition-all duration-150 placeholder:text-gray-400"
                    placeholder="you@company.com"
                  />
                </div>
              </div>

              <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div>
                  <label for="company" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3">Company</label>
                  <input
                    type="text"
                    id="company"
                    bind:value={formData.company}
                    required
                    class="w-full px-4 py-4 bg-gray-50 border border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy focus:bg-white transition-all duration-150 placeholder:text-gray-400"
                    placeholder="Company name"
                  />
                </div>
                <div>
                  <label for="need" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3">Primary Need</label>
                  <div class="relative">
                    <select
                      id="need"
                      bind:value={formData.need}
                      required
                      class="w-full px-4 py-4 pr-12 border text-base font-light focus:outline-none transition-all duration-150 cursor-pointer appearance-none {formData.need === 'manufacturing' ? 'text-navy bg-navy-100 border-navy/20' : formData.need === 'distribution' ? 'text-teal bg-teal-100 border-teal/20' : 'text-navy bg-gray-50 border-gray-200 focus:border-navy focus:bg-white'}"
                    >
                      <option value="" disabled>Select one</option>
                      <option value="manufacturing">Manufacturing</option>
                      <option value="distribution">Distribution</option>
                      <option value="both">Both</option>
                      <option value="other">Other</option>
                    </select>
                    <div class="absolute right-4 top-1/2 -translate-y-1/2 pointer-events-none">
                      <svg class="w-5 h-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M19 9l-7 7-7-7" />
                      </svg>
                    </div>
                  </div>
                </div>
              </div>

              <div>
                <label for="message" class="block text-xs tracking-widest uppercase text-gray-400 font-medium mb-3">Tell us about your challenge</label>
                <textarea
                  id="message"
                  bind:value={formData.message}
                  required
                  rows="5"
                  minlength="20"
                  class="w-full px-4 py-4 bg-gray-50 border border-gray-200 text-navy text-base font-light focus:outline-none focus:border-navy focus:bg-white transition-all duration-150 placeholder:text-gray-400 resize-none"
                  placeholder="What challenges are you facing with manufacturing or distribution?"
                ></textarea>
              </div>

              <div class="pt-4">
                <button
                  type="submit"
                  disabled={isSubmitting}
                  class="px-10 py-4 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150 disabled:opacity-50 disabled:cursor-not-allowed"
                >
                  {isSubmitting ? 'Sending...' : 'Send Message'}
                </button>
              </div>
            </form>
          {/if}
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-navy text-white">
    <!-- Main Footer -->
    <div class="py-16 md:py-20">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
        <div class="grid grid-cols-2 md:grid-cols-5 gap-10 md:gap-8">
        <!-- Logo -->
        <div class="col-span-2 md:col-span-2">
          <img src="/logo-footer.svg" alt="CG Operating Group" class="h-10 brightness-0 invert" />
        </div>

        <!-- Navigate -->
        <div>
          <p class="text-xs tracking-wider text-white/40 mb-5">Navigate</p>
          <nav class="flex flex-col gap-2.5">
            <a href="/needs" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Your Needs</a>
            <a href="/impact" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Our Impact</a>
            <a href="/firm" class="text-sm text-white/70 hover:text-white transition-colors duration-150">The Firm</a>
          </nav>
        </div>

        <!-- Services -->
        <div>
          <p class="text-xs tracking-wider text-white/40 mb-5">Services</p>
          <nav class="flex flex-col gap-2.5">
            <a href="/needs" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Manufacturing</a>
            <a href="/needs" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Distribution</a>
          </nav>
        </div>

        <!-- Connect -->
        <div>
          <p class="text-xs tracking-wider text-white/40 mb-5">Connect</p>
          <nav class="flex flex-col gap-2.5">
            <a href="mailto:contact@cgoperatinggroup.com" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Email</a>
            <a href="https://linkedin.com" class="text-sm text-white/70 hover:text-white transition-colors duration-150">LinkedIn</a>
          </nav>
        </div>
        </div>
      </div>
    </div>

    <!-- Footer Bottom -->
    <div class="py-5 border-t border-white/10">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
        <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-3">
          <p class="text-xs text-white/40">© 2025 CG Operating Group</p>
          <p class="text-xs text-white/40">Manufacturing & Distribution Infrastructure</p>
        </div>
      </div>
    </div>
  </footer>

</main>
