<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import { page } from '$app/stores';
  import { goto } from '$app/navigation';

  $: activeTab = ($page.url.searchParams.get('tab') as 'manufacturing' | 'distribution') || 'manufacturing';

  function setTab(tab: 'manufacturing' | 'distribution') {
    goto(`?tab=${tab}`, { replaceState: true, noScroll: true });
  }
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero -->
  <div class="py-16 md:py-24">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Your Needs</p>
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-black leading-[1.15] max-w-4xl">
        Two capabilities. One infrastructure.
      </h1>
      <p class="mt-6 text-xl md:text-2xl text-gray-500 font-light leading-relaxed max-w-2xl">
        Choose your path: precision <span class="text-navy font-normal">manufacturing</span> or strategic <span class="text-teal font-normal">distribution</span>.
      </p>
    </div>
  </div>

  <!-- Tabs -->
  <div class="border-t border-b border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="flex gap-0">
        <button
          on:click={() => setTab('manufacturing')}
          class="py-5 px-6 text-base font-medium tracking-wide transition-all duration-150 cursor-pointer border-b-2 -mb-[1px] {activeTab === 'manufacturing' ? 'text-navy border-navy' : 'text-gray-400 hover:text-gray-600 border-transparent'}"
        >
          Manufacturing
        </button>
        <button
          on:click={() => setTab('distribution')}
          class="py-5 px-6 text-base font-medium tracking-wide transition-all duration-150 cursor-pointer border-b-2 -mb-[1px] {activeTab === 'distribution' ? 'text-teal border-teal' : 'text-gray-400 hover:text-gray-600 border-transparent'}"
        >
          Distribution
        </button>
      </div>
    </div>
  </div>

  <!-- Manufacturing Content -->
  {#if activeTab === 'manufacturing'}
    <div class="py-16 md:py-24">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">

        <!-- Intro -->
        <div class="max-w-4xl mb-16">
          <p class="text-xl md:text-2xl text-gray-600 font-light leading-relaxed">
            CG Operating Group delivers end-to-end manufacturing oversight built for brands that need accuracy, speed, and clarity across their production lines. Our role is not to source a factory. It is to create a <span class="text-navy font-normal">controlled manufacturing environment</span> that produces consistent output at competitive cost while removing the weak points that normally drain margin and slow teams down.
          </p>
        </div>

        <!-- Main Content Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 lg:gap-24">

          <!-- Left Column -->
          <div class="space-y-8">
            <div>
              <h3 class="text-sm tracking-widest uppercase text-navy font-medium mb-4">Global Factory Network</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                We work through a vetted global network of factories, built through years of direct relationships and on-the-ground experience. Each partner is selected for reliability, capacity, and alignment with the quality expectations of leading brands.
              </p>
            </div>

            <div>
              <h3 class="text-sm tracking-widest uppercase text-navy font-medium mb-4">Direct Pricing & Clean Pathways</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                By matching products to the right factory class, negotiating direct volume-based pricing, and structuring clean production pathways, we give brands access to stable and efficient manufacturing without the uncertainty that usually comes with overseas work.
              </p>
            </div>

            <div>
              <h3 class="text-sm tracking-widest uppercase text-navy font-medium mb-4">Full Production Lifecycle</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                Our team manages the full production lifecycle at the factory level. This includes pre-production planning, material sourcing, sampling, line setup, timeline control, communication with factory leadership, and quality checks at every meaningful stage, ending with a final inspection before goods move to freight. This approach shortens lead times, prevents avoidable errors, and keeps production aligned with the standards set at the beginning of each run.
              </p>
            </div>
          </div>

          <!-- Right Column -->
          <div class="space-y-8">
            <div>
              <h3 class="text-sm tracking-widest uppercase text-navy font-medium mb-4">Leak Prevention</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                Leak prevention is part of the system, not the headline. We structure production so product stays contained, specifications are protected, and output goes where it is supposed to go. It is one of several controls we put in place to keep operations clean and predictable.
              </p>
            </div>

            <div>
              <h3 class="text-sm tracking-widest uppercase text-navy font-medium mb-4">The Core Advantage</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                The core advantage of our model is simple. We compete on cost, improve efficiency, and clean up the operational mess that slows brands down. Instead of managing inflated layers, inconsistent partners, and unpredictable timelines, companies get a manufacturing engine that moves the way it should.
              </p>
            </div>

            <div>
              <h3 class="text-sm tracking-widest uppercase text-navy font-medium mb-4">Scale Ready</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                By operating directly inside the production environment, we remove miscommunication, reduce idle cycles, and deliver faster, more consistent output. As companies scale, we secure capacity, plan for higher volumes, and maintain standards so growth does not come with operational drag.
              </p>
            </div>
          </div>

        </div>

        <!-- Bottom Highlight -->
        <div class="mt-16 p-10 md:p-12 bg-navy text-white">
          <p class="text-xl md:text-2xl font-light leading-relaxed max-w-3xl">
            This is manufacturing built for speed, cost efficiency, and real control. It replaces chaos with structure and gives brands the clarity they need to grow.
          </p>
          <a href="/contact?need=manufacturing" class="inline-block mt-8 px-8 py-4 bg-white text-navy text-sm font-medium tracking-wide hover:bg-gray-100 transition-colors duration-150">
            Discuss Manufacturing
          </a>
        </div>

      </div>
    </div>
  {/if}

  <!-- Distribution Content -->
  {#if activeTab === 'distribution'}
    <div class="py-16 md:py-24">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">

        <!-- Intro -->
        <div class="max-w-4xl mb-16">
          <p class="text-xl md:text-2xl text-gray-600 font-light leading-relaxed">
            CG Operating Group manages a distribution ecosystem built for brands that need their product to move with clarity and pace. Our work focuses on reach, speed, and strategic placement, making sure goods land where they create momentum instead of friction. The objective is straightforward: <span class="text-teal font-normal">move product in a way that supports the company's larger commercial goals</span>.
          </p>
        </div>

        <!-- Main Content Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 lg:gap-24">

          <!-- Left Column -->
          <div class="space-y-8">
            <div>
              <h3 class="text-sm tracking-widest uppercase text-teal font-medium mb-4">Proven Network</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                Our network spans partners and channels that have demonstrated real capacity across apparel, footwear, accessories, and consumer goods. These relationships were built through consistent output and hands-on execution, not theory. Working within this ecosystem allows us to direct product with intention rather than rely on the chaotic and inconsistent paths that often define secondary distribution.
              </p>
            </div>

            <div>
              <h3 class="text-sm tracking-widest uppercase text-teal font-medium mb-4">Disciplined Approach</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                What defines our approach is the discipline behind it. We look at where the product should go, how it should move, and what cadence makes the most sense for the brand's next phase of growth. Our team handles allocation, channel fit, pricing expectations, and volume planning so distribution functions as a coordinated system rather than a series of one-off transactions.
              </p>
            </div>

            <div>
              <h3 class="text-sm tracking-widest uppercase text-teal font-medium mb-4">Immediate Value</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                The value is immediate. We move more of your product, at a faster and more consistent pace, through channels built to handle real volume. Companies gain meaningful output without the confusion, delays, or fragmented processes that usually slow distribution down. Movement becomes reliable. Scaling becomes realistic and partnership becomes a no-brainer.
              </p>
            </div>
          </div>

          <!-- Right Column - Ways to Work -->
          <div>
            <h3 class="text-sm tracking-widest uppercase text-gray-400 font-medium mb-8">Ways to Work With Us</h3>

            <div class="space-y-8">
              <div class="flex gap-6">
                <div class="text-3xl font-light text-teal">01</div>
                <div>
                  <p class="text-navy font-medium mb-2">Ongoing Distribution Partnerships</p>
                  <p class="text-gray-600 font-light leading-relaxed">
                    Some brands engage through ongoing distribution partnerships that create steady, predictable movement.
                  </p>
                </div>
              </div>

              <div class="flex gap-6">
                <div class="text-3xl font-light text-teal">02</div>
                <div>
                  <p class="text-navy font-medium mb-2">Deal-by-Deal Placements</p>
                  <p class="text-gray-600 font-light leading-relaxed">
                    Others prefer deal-by-deal placements when speed, flexibility, or targeted exposure is the priority.
                  </p>
                </div>
              </div>

              <div class="flex gap-6">
                <div class="text-3xl font-light text-teal">03</div>
                <div>
                  <p class="text-navy font-medium mb-2">Discreet Liquidation</p>
                  <p class="text-gray-600 font-light leading-relaxed">
                    When inventory needs to move outside normal retail rhythms, we provide discreet and efficient liquidation routes that resolve the issue cleanly while keeping everything aligned with the brand's broader commercial objectives.
                  </p>
                </div>
              </div>
            </div>

            <div class="mt-12 pt-8 border-t border-gray-100">
              <h3 class="text-sm tracking-widest uppercase text-teal font-medium mb-4">Scale Ready</h3>
              <p class="text-gray-600 font-light leading-relaxed">
                As brands grow, our system grows with them. We secure capacity in advance, prepare channels for higher volume, and maintain the consistency that high-growth companies rarely get from downstream partners.
              </p>
            </div>
          </div>

        </div>

        <!-- Bottom Highlight -->
        <div class="mt-16 p-10 md:p-12 bg-teal text-white">
          <p class="text-xl md:text-2xl font-light leading-relaxed max-w-3xl">
            This is distribution built with intention. It moves product decisively, adapts to the moment, and gives companies the confidence that comes from having real structure behind their downstream operations.
          </p>
          <a href="/contact?need=distribution" class="inline-block mt-8 px-8 py-4 bg-white text-teal text-sm font-medium tracking-wide hover:bg-gray-100 transition-colors duration-150">
            Discuss Distribution
          </a>
        </div>

      </div>
    </div>
  {/if}

  <!-- CTA -->
  <div class="py-24 md:py-32 border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">
        <div class="lg:col-span-7">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Get Started</p>
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy leading-tight tracking-tight max-w-2xl">
            Ready to discuss your needs?
          </h2>
        </div>
        <div class="lg:col-span-5 flex flex-col justify-end">
          <p class="text-gray-500 font-light text-lg leading-relaxed mb-8">
            Tell us about your challenge. We'll tell you if we're the right fit. No sales pitch. No obligation.
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="/contact" class="px-8 py-4 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150 text-center">
              Start a Conversation
            </a>
            <a href="/impact" class="px-8 py-4 border border-gray-300 text-navy text-sm font-medium tracking-wide hover:border-navy hover:bg-navy hover:text-white transition-all duration-150 text-center">
              See Our Impact
            </a>
          </div>
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
            <a href="/firm" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Our Firm</a>
          </nav>
        </div>

        <!-- Services -->
        <div>
          <p class="text-xs tracking-wider text-white/40 mb-5">Services</p>
          <nav class="flex flex-col gap-2.5">
            <a href="/needs?tab=manufacturing" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Manufacturing</a>
            <a href="/needs?tab=distribution" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Distribution</a>
          </nav>
        </div>

        <!-- Connect -->
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

    <!-- Footer Bottom -->
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
