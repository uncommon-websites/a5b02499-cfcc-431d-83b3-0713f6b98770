<script lang="ts">
  import Header from "$lib/components/Header.svelte";
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero -->
  <div class="py-16 md:py-24">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Our Firm</p>
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-black leading-[1.15] max-w-3xl">
        The partners behind the operation.
      </h1>
    </div>
  </div>

  <!-- Partner 1 - Gabe Gorman -->
  <div class="border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="py-16 md:py-24 grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">

        <!-- Image -->
        <div class="lg:col-span-5">
          <img src="/gabe-gorman.webp" alt="Gabe Gorman" class="w-full aspect-[2/3] object-cover" />
        </div>

        <!-- Bio -->
        <div class="lg:col-span-7 flex flex-col justify-center">
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy tracking-tight mb-2">
            Gabe Gorman
          </h2>
          <p class="text-sm tracking-widest uppercase text-navy font-medium mb-8">Managing Partner</p>

          <div class="space-y-6 text-gray-600 text-base md:text-lg font-light leading-relaxed">
            <p>
              Gabe entered the business world after completing his military service, where he developed the discipline and operational mindset that would later define his career. He began in real estate, acquiring and flipping residential properties. The work exposed a glaring truth: the cost of materials was wildly inflated compared to their true raw value. That sparked a deeper investigation into global sourcing, manufacturing economics, and how products really move through a supply chain.
            </p>
            <p>
              That curiosity turned into capability. Gabe transitioned into large-scale sourcing work within the reselling ecosystem, becoming the core operator behind one of the nation's largest sneaker communities. He managed procurement pipelines supplying tens of thousands of members, coordinating constant product flow, negotiating with suppliers, and solving the types of logistical problems most teams aren't built to handle.
            </p>
            <p>
              In the process, he built a hardened network of overseas factory relationships, freight partners, and sourcing channels that now serve as foundational infrastructure for CG Operating Group. Gabe oversees global sourcing, factory alignment, and international operations, bringing a level of <span class="text-navy font-normal">cost discipline and supply-chain visibility</span> that brands rarely ever experience.
            </p>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- Partner 2 - Jacob Canner -->
  <div class="border-t border-gray-100 bg-gray-50">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="py-16 md:py-24 grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">

        <!-- Image - Order changes on mobile vs desktop -->
        <div class="lg:col-span-5 lg:order-2">
          <img src="/jacob-canner.webp" alt="Jacob Canner" class="w-full aspect-[2/3] object-cover" />
        </div>

        <!-- Bio -->
        <div class="lg:col-span-7 lg:order-1 flex flex-col justify-center">
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy tracking-tight mb-2">
            Jacob Canner
          </h2>
          <p class="text-sm tracking-widest uppercase text-teal font-medium mb-8">Managing Partner</p>

          <div class="space-y-6 text-gray-600 text-base md:text-lg font-light leading-relaxed">
            <p>
              Jacob started reselling sneakers as a freshman in high school, turning a small hustle into one of the largest apparel-selling pipelines on StockX. Managing constant volume across multiple categories gave him a ground-level view into pricing behavior, demand patterns, and how inefficient most distribution structures actually are.
            </p>
            <p>
              As he scaled, he kept running into the same problem: brands were losing margin and time to bloated supply chains that couldn't keep up with real market velocity. That pushed him upstream into manufacturing, where he began working directly with factories to understand true production costs, cut out unnecessary intermediaries, and bring clarity to a system built on guesswork.
            </p>
            <p>
              Today, Jacob brings that combination of large-volume distribution experience and factory-level insight to CG Operating Group. His focus is improving cost structures, stabilizing production, and building <span class="text-teal font-normal">high-volume distribution pathways</span> that let brands grow without dragging their own operations behind them.
            </p>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- CTA -->
  <div class="py-24 md:py-32 border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">
        <div class="lg:col-span-7">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Work With Us</p>
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy leading-tight tracking-tight max-w-2xl">
            Ready to work with us?
          </h2>
        </div>
        <div class="lg:col-span-5 flex flex-col justify-end">
          <p class="text-gray-500 font-light text-lg leading-relaxed mb-8">
            We take on a limited number of engagements each year to ensure every client gets the attention they deserve.
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="/contact" class="px-8 py-4 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150 text-center">
              Get in Touch
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
            <a href="/needs" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Manufacturing</a>
            <a href="/needs" class="text-sm text-white/70 hover:text-white transition-colors duration-150">Distribution</a>
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
