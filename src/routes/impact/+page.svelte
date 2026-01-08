<script lang="ts">
  import Header from "$lib/components/Header.svelte";
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero -->
  <div class="py-16 md:py-24">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="max-w-4xl">
        <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Our Impact</p>
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-black leading-[1.15]">
          Results that speak for themselves.
        </h1>
        <p class="mt-6 text-xl md:text-2xl text-gray-500 font-light leading-relaxed max-w-2xl">
          We measure success by the tangible outcomes we deliver for our partners.
        </p>
      </div>
    </div>
  </div>

  <!-- Two Column Impact Sections -->
  <div class="border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2">

        <!-- Manufacturing Column -->
        <div class="py-16 md:py-24 lg:pr-16 xl:pr-24 lg:border-r border-gray-100 flex flex-col">
          <div class="flex items-center gap-4 mb-10">
            <div class="w-3 h-3 bg-navy"></div>
            <h2 class="text-xs tracking-widest uppercase text-navy font-medium">Manufacturing</h2>
          </div>

          <div class="space-y-8 flex-1">
            <div class="group">
              <div class="flex gap-4">
                <div class="shrink-0 w-1.5 h-1.5 bg-navy/40 rounded-full mt-3"></div>
                <p class="text-lg md:text-xl text-gray-700 font-light leading-relaxed">
                  Removed supply-chain leakages and upgraded quality for a hat brand moving <span class="text-navy font-normal">100,000+ units monthly</span>.
                </p>
              </div>
            </div>

            <div class="group">
              <div class="flex gap-4">
                <div class="shrink-0 w-1.5 h-1.5 bg-navy/40 rounded-full mt-3"></div>
                <p class="text-lg md:text-xl text-gray-700 font-light leading-relaxed">
                  Beat cost and improved quality for a <span class="text-navy font-normal">global athletic brand</span>, while expanding multi-country distribution.
                </p>
              </div>
            </div>
          </div>

          <!-- Manufacturing Stats -->
          <div class="mt-auto pt-10 border-t border-gray-100">
            <div class="grid grid-cols-2 gap-8">
              <div>
                <p class="text-4xl md:text-5xl font-light text-navy tracking-tight">100K+</p>
                <p class="text-sm text-gray-500 mt-2 font-light">Units monthly</p>
              </div>
              <div>
                <p class="text-4xl md:text-5xl font-light text-navy tracking-tight">Global</p>
                <p class="text-sm text-gray-500 mt-2 font-light">Production reach</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Distribution Column -->
        <div class="py-16 md:py-24 lg:pl-16 xl:pl-24 border-t lg:border-t-0 border-gray-100 flex flex-col">
          <div class="flex items-center gap-4 mb-10">
            <div class="w-3 h-3 bg-teal"></div>
            <h2 class="text-xs tracking-widest uppercase text-teal font-medium">Distribution</h2>
          </div>

          <div class="space-y-8 flex-1">
            <div class="group">
              <div class="flex gap-4">
                <div class="shrink-0 w-1.5 h-1.5 bg-teal/40 rounded-full mt-3"></div>
                <p class="text-lg md:text-xl text-gray-700 font-light leading-relaxed">
                  Scaled an eBay store to <span class="text-teal font-normal">thousands of reviews</span>.
                </p>
              </div>
            </div>

            <div class="group">
              <div class="flex gap-4">
                <div class="shrink-0 w-1.5 h-1.5 bg-teal/40 rounded-full mt-3"></div>
                <p class="text-lg md:text-xl text-gray-700 font-light leading-relaxed">
                  Performed in the <span class="text-teal font-normal">top tier on Whatnot</span>.
                </p>
              </div>
            </div>

            <div class="group">
              <div class="flex gap-4">
                <div class="shrink-0 w-1.5 h-1.5 bg-teal/40 rounded-full mt-3"></div>
                <p class="text-lg md:text-xl text-gray-700 font-light leading-relaxed">
                  Ranked as a <span class="text-teal font-normal">top seller on StockX</span>.
                </p>
              </div>
            </div>

            <div class="group">
              <div class="flex gap-4">
                <div class="shrink-0 w-1.5 h-1.5 bg-teal/40 rounded-full mt-3"></div>
                <p class="text-lg md:text-xl text-gray-700 font-light leading-relaxed">
                  Ranked <span class="text-teal font-normal">sub 60 on TikTok Shop</span> globally.
                </p>
              </div>
            </div>
          </div>

          <!-- Distribution Stats -->
          <div class="mt-auto pt-10 border-t border-gray-100">
            <div class="grid grid-cols-2 gap-8">
              <div>
                <p class="text-4xl md:text-5xl font-light text-teal tracking-tight">Top 60</p>
                <p class="text-sm text-gray-500 mt-2 font-light">TikTok Shop rank</p>
              </div>
              <div>
                <p class="text-4xl md:text-5xl font-light text-teal tracking-tight">10+</p>
                <p class="text-sm text-gray-500 mt-2 font-light">Active channels</p>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- Platform Logos / Credibility Strip -->
  <div class="py-16 md:py-20 bg-gray-50">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <p class="text-xs tracking-widest uppercase text-gray-400 font-medium text-center mb-10">Active Across Major Platforms</p>
      <div class="flex flex-wrap justify-center items-center gap-8 md:gap-16">
        <span class="text-xl md:text-2xl font-light text-gray-400 tracking-tight">StockX</span>
        <span class="text-xl md:text-2xl font-light text-gray-400 tracking-tight">TikTok Shop</span>
        <span class="text-xl md:text-2xl font-light text-gray-400 tracking-tight">eBay</span>
        <span class="text-xl md:text-2xl font-light text-gray-400 tracking-tight">Whatnot</span>
      </div>
    </div>
  </div>

  <!-- CTA -->
  <div class="py-24 md:py-32 border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">
        <div class="lg:col-span-7">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Your Turn</p>
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy leading-tight tracking-tight max-w-2xl">
            Ready for your transformation?
          </h2>
        </div>
        <div class="lg:col-span-5 flex flex-col justify-end">
          <p class="text-gray-500 font-light text-lg leading-relaxed mb-8">
            These results aren't outliers. They're what happens when you work with experienced operators.
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="/contact" class="px-8 py-4 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150 text-center">
              Start Your Transformation
            </a>
            <a href="/needs" class="px-8 py-4 border border-gray-300 text-navy text-sm font-medium tracking-wide hover:border-navy hover:bg-navy hover:text-white transition-all duration-150 text-center">
              Explore Services
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
