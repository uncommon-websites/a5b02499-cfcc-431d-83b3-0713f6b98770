<script lang="ts">
  import Header from "$lib/components/Header.svelte";

  const impacts = [
    {
      number: "01",
      text: "Scaled an eBay store past 10,000 reviews through consistent volume.",
      type: "distribution"
    },
    {
      number: "02",
      text: "Performed in the top tier on Whatnot.",
      type: "distribution"
    },
    {
      number: "03",
      text: "Ranked as the top apparel seller on StockX in 2024.",
      type: "distribution"
    },
    {
      number: "04",
      text: "Ranked 52nd on TikTok Shop in October 2025.",
      type: "distribution"
    },
    {
      number: "05",
      text: "Launched two DTC brands.",
      type: "distribution"
    },
    {
      number: "06",
      text: "Cut a hat brand's production costs, removed supply-chain leakages, and upgraded quality for an operation moving over 100,000 units per month.",
      type: "manufacturing"
    },
    {
      number: "07",
      text: "Improved manufacturing consistency and expanded multi-country distribution for a global athletic brand moving several million units per year.",
      type: "both"
    }
  ];
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero -->
  <div class="py-20 md:py-32">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16">
        <div class="lg:col-span-3">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium">Our Impact</p>
        </div>
        <div class="lg:col-span-9">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-gray-500 leading-[1.2] max-w-4xl">
            Real transformations. Measurable results. Our work speaks for itself.
          </h1>
        </div>
      </div>
    </div>
  </div>

  <!-- Impact Items -->
  <div class="border-t border-gray-100">
    <div class="max-w-[1600px] mx-auto">
      {#each impacts as impact, i}
        <div
          class="py-10 md:py-12 border-b border-gray-100 px-6 md:px-16 lg:px-24 -mx-0 transition-colors duration-150 cursor-default min-h-[160px] md:min-h-[180px] flex items-center {impact.type === 'manufacturing' ? 'hover:bg-navy hover:text-white' : impact.type === 'distribution' ? 'hover:bg-teal hover:text-white' : 'hover:bg-navy hover:text-white'} group"
        >
          <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 lg:gap-16 items-center w-full">
            <div class="lg:col-span-2">
              <span class="text-3xl md:text-4xl font-light transition-colors duration-150 {impact.type === 'manufacturing' ? 'text-navy group-hover:text-white' : impact.type === 'distribution' ? 'text-teal group-hover:text-white' : 'text-navy group-hover:text-white'}">
                {impact.number}
              </span>
            </div>
            <div class="lg:col-span-8">
              <p class="text-xl md:text-2xl lg:text-3xl font-light text-navy leading-relaxed tracking-tight transition-colors duration-150 group-hover:text-white">
                {impact.text}
              </p>
            </div>
            <div class="lg:col-span-2 flex justify-end">
              <span class="text-xs tracking-widest uppercase font-medium whitespace-nowrap transition-colors duration-150 {impact.type === 'manufacturing' ? 'text-navy group-hover:text-white/70' : impact.type === 'distribution' ? 'text-teal group-hover:text-white/70' : 'text-gray-400 group-hover:text-white/70'}">
                {impact.type === 'both' ? 'Mfg + Dist' : impact.type === 'manufacturing' ? 'Mfg' : 'Dist'}
              </span>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>

  <!-- Stats -->
  <div class="py-20 md:py-28 bg-gray-50">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 md:gap-12 text-center">
        <div>
          <p class="text-4xl md:text-5xl lg:text-6xl font-light text-navy tracking-tight">10K+</p>
          <p class="text-sm text-gray-500 mt-2 font-light">eBay reviews</p>
        </div>
        <div>
          <p class="text-4xl md:text-5xl lg:text-6xl font-light text-teal tracking-tight">#1</p>
          <p class="text-sm text-gray-500 mt-2 font-light">StockX apparel seller</p>
        </div>
        <div>
          <p class="text-4xl md:text-5xl lg:text-6xl font-light text-navy tracking-tight">100K+</p>
          <p class="text-sm text-gray-500 mt-2 font-light">Units monthly</p>
        </div>
        <div>
          <p class="text-4xl md:text-5xl lg:text-6xl font-light text-teal tracking-tight">#52</p>
          <p class="text-sm text-gray-500 mt-2 font-light">TikTok Shop ranking</p>
        </div>
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
            <a href="/firm" class="text-sm text-white/70 hover:text-white transition-colors duration-150">The Firm</a>
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
