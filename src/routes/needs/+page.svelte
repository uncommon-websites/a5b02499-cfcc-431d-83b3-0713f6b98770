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
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16">
        <div class="lg:col-span-3">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium">Your Needs</p>
        </div>
        <div class="lg:col-span-9">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-gray-500 leading-[1.2] max-w-5xl text-balance">
            Choose your path: precision <mark class="bg-navy/10 text-navy px-1">manufacturing</mark> or strategic <mark class="bg-teal/15 text-teal px-1">distribution</mark>.
          </h1>
        </div>
      </div>
    </div>
  </div>

  <!-- Tabs -->
  <div class="border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="flex gap-8">
        <button
          on:click={() => setTab('manufacturing')}
          class="py-6 text-lg font-light tracking-tight transition-colors duration-150 cursor-pointer {activeTab === 'manufacturing' ? 'text-navy' : 'text-gray-400 hover:text-gray-600'}"
        >
          Manufacturing
        </button>
        <button
          on:click={() => setTab('distribution')}
          class="py-6 text-lg font-light tracking-tight transition-colors duration-150 cursor-pointer {activeTab === 'distribution' ? 'text-teal' : 'text-gray-400 hover:text-gray-600'}"
        >
          Distribution
        </button>
      </div>
    </div>
  </div>

  <!-- Manufacturing Content -->
  {#if activeTab === 'manufacturing'}
    <div class="py-16 md:py-24 bg-navy-50">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16">

          <!-- Left Column -->
          <div class="lg:col-span-4">
            <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy tracking-tight leading-tight mb-6">
              End-to-End Oversight.
            </h2>
            <p class="text-gray-500 font-light leading-relaxed mb-8">
              A controlled manufacturing environment that produces consistent output at competitive cost.
            </p>
            <a href="/contact?need=manufacturing" class="inline-block px-6 py-3 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150">
              Discuss Manufacturing
            </a>
          </div>

          <!-- Right Column - Content -->
          <div class="lg:col-span-8">
            <div class="space-y-6 text-gray-600 text-base md:text-lg font-light leading-relaxed">
              <p>
                CG Operating Group delivers end-to-end manufacturing oversight built for brands that need accuracy, speed, and clarity across their production lines. Our role is not to source a factory. It is to create a controlled manufacturing environment that produces consistent output at competitive cost while removing the weak points that normally drain margin and slow teams down.
              </p>
              <p>
                We work through a vetted global network of factories, built through years of direct relationships and on-the-ground experience. Each partner is selected for reliability, capacity, and alignment with the quality expectations of leading brands. By matching products to the right factory class, negotiating direct volume-based pricing, and structuring clean production pathways, we give brands access to stable and efficient manufacturing without the uncertainty that usually comes with overseas work.
              </p>
              <p>
                Our team manages the full production lifecycle at the factory level. This includes pre-production planning, material sourcing, sampling, line setup, timeline control, communication with factory leadership, and quality checks at every meaningful stage, ending with a final inspection before goods move to freight.
              </p>
            </div>

            <!-- Key Points -->
            <div class="mt-12 pt-12 border-t border-gray-200">
              <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div>
                  <p class="text-sm tracking-widest uppercase text-navy font-medium mb-3">Leak Prevention</p>
                  <p class="text-gray-500 font-light leading-relaxed">
                    We structure production so product stays contained, specifications are protected, and output goes where it is supposed to go.
                  </p>
                </div>
                <div>
                  <p class="text-sm tracking-widest uppercase text-navy font-medium mb-3">Scale Ready</p>
                  <p class="text-gray-500 font-light leading-relaxed">
                    As companies scale, we secure capacity, plan for higher volumes, and maintain standards so growth does not come with operational drag.
                  </p>
                </div>
              </div>
            </div>

            <!-- Quote/Highlight -->
            <div class="mt-12 p-8 md:p-10 bg-navy text-white">
              <p class="text-xl md:text-2xl font-light leading-relaxed">
                "We compete on cost, improve efficiency, and clean up the operational mess that slows brands down."
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  {/if}

  <!-- Distribution Content -->
  {#if activeTab === 'distribution'}
    <div class="py-16 md:py-24 bg-teal-50">
      <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16">

          <!-- Left Column -->
          <div class="lg:col-span-4">
            <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy tracking-tight leading-tight mb-6">
              Clear, Paced Movement.
            </h2>
            <p class="text-gray-500 font-light leading-relaxed mb-8">
              A distribution ecosystem built for brands that need their product to move with clarity and pace.
            </p>
            <a href="/contact?need=distribution" class="inline-block px-6 py-3 bg-teal text-white text-sm font-medium tracking-wide hover:bg-teal-500 transition-colors duration-150">
              Discuss Distribution
            </a>
          </div>

          <!-- Right Column - Content -->
          <div class="lg:col-span-8">
            <div class="space-y-6 text-gray-600 text-base md:text-lg font-light leading-relaxed">
              <p>
                CG Operating Group manages a distribution ecosystem built for brands that need their product to move with clarity and pace. Our work focuses on reach, speed, and strategic placement, making sure goods land where they create momentum instead of friction. The objective is straightforward: move product in a way that supports the company's larger commercial goals.
              </p>
              <p>
                Our network spans partners and channels that have demonstrated real capacity across apparel, footwear, accessories, and consumer goods. These relationships were built through consistent output and hands-on execution, not theory. Working within this ecosystem allows us to direct product with intention rather than rely on the chaotic and inconsistent paths that often define secondary distribution.
              </p>
              <p>
                What defines our approach is the discipline behind it. We look at where the product should go, how it should move, and what cadence makes the most sense for the brand's next phase of growth. Our team handles allocation, channel fit, pricing expectations, and volume planning so distribution functions as a coordinated system rather than a series of one-off transactions.
              </p>
            </div>

            <!-- Ways to Work -->
            <div class="mt-12 pt-12 border-t border-gray-100">
              <p class="text-sm tracking-widest uppercase text-gray-400 font-medium mb-8">Ways to Work With Us</p>
              <div class="space-y-6">
                <div class="flex gap-6">
                  <div class="text-2xl font-light text-teal">01</div>
                  <div>
                    <p class="text-navy font-medium mb-1">Ongoing Partnerships</p>
                    <p class="text-gray-500 font-light">Steady, predictable movement through consistent distribution relationships.</p>
                  </div>
                </div>
                <div class="flex gap-6">
                  <div class="text-2xl font-light text-teal">02</div>
                  <div>
                    <p class="text-navy font-medium mb-1">Deal-by-Deal Placements</p>
                    <p class="text-gray-500 font-light">Speed, flexibility, or targeted exposure when the situation calls for it.</p>
                  </div>
                </div>
                <div class="flex gap-6">
                  <div class="text-2xl font-light text-teal">03</div>
                  <div>
                    <p class="text-navy font-medium mb-1">Discreet Liquidation</p>
                    <p class="text-gray-500 font-light">Efficient routes that resolve inventory cleanly while staying aligned with brand objectives.</p>
                  </div>
                </div>
              </div>
            </div>

            <!-- Quote/Highlight -->
            <div class="mt-12 p-8 md:p-10 bg-teal text-white">
              <p class="text-xl md:text-2xl font-light leading-relaxed">
                "We move more of your product, at a faster and more consistent pace, through channels built to handle real volume."
              </p>
            </div>
          </div>
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
