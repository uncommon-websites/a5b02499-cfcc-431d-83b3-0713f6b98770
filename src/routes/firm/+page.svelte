<script lang="ts">
  import Header from "$lib/components/Header.svelte";
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero -->
  <div class="py-20 md:py-32">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16">
        <div class="lg:col-span-3">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium">The Firm</p>
        </div>
        <div class="lg:col-span-9">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-light tracking-tight text-navy leading-[1.1] max-w-3xl">
            The Partners.
          </h1>
          <p class="mt-6 text-xl md:text-2xl text-gray-400 font-light max-w-2xl leading-relaxed">
            We are a private partnership. You do not deal with account managers. You deal with the operators.
          </p>
        </div>
      </div>
    </div>
  </div>

  <!-- Partners -->
  <div class="border-t border-gray-100">
    <div class="max-w-[1600px] mx-auto">

      <!-- Partner 1 - Gabe Gorman -->
      <div class="py-16 md:py-20 border-b border-gray-100 px-6 md:px-16 lg:px-24 group hover:bg-navy transition-colors duration-300">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16 items-start">
          <div class="lg:col-span-4">
            <div class="aspect-[4/5] overflow-hidden max-w-[300px]">
              <img src="/gabe-gorman.webp" alt="Gabe Gorman" class="w-full h-full object-cover transition-all duration-500 saturate-0 contrast-[1.1] group-hover:saturate-100 group-hover:contrast-100" />
            </div>
          </div>
          <div class="lg:col-span-8">
            <p class="text-xs tracking-widest uppercase text-gray-400 group-hover:text-white/50 font-medium mb-2 transition-colors duration-300">Founding Partner</p>
            <h2 class="text-2xl md:text-3xl lg:text-4xl font-light text-navy group-hover:text-white tracking-tight transition-colors duration-300 mb-2">
              Gabe Gorman
            </h2>
            <p class="text-sm tracking-widest uppercase text-navy group-hover:text-white/70 font-medium mb-6 transition-colors duration-300">Global Manufacturing & Supply Chain</p>
            <p class="text-base md:text-lg text-gray-500 group-hover:text-white/80 font-light leading-relaxed transition-colors duration-300 max-w-xl mb-4">
              20+ years building and optimizing manufacturing operations for Fortune 500 companies. Expert in procurement, quality control, and production systems that scale without capital expansion.
            </p>
            <p class="text-base md:text-lg text-gray-500 group-hover:text-white/80 font-light leading-relaxed transition-colors duration-300 max-w-xl">
              Gabe built overseas factory networks through military discipline and large-scale sneaker sourcing. His hands-on supply chain experience eliminates the cost inflation and logistical chaos brands face when scaling manufacturing operations globally.
            </p>
          </div>
        </div>
      </div>

      <!-- Partner 2 - Jacob Canner -->
      <div class="py-16 md:py-20 border-b border-gray-100 px-6 md:px-16 lg:px-24 group hover:bg-teal transition-colors duration-300">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16 items-start">
          <div class="lg:col-span-4">
            <div class="aspect-[4/5] overflow-hidden max-w-[300px]">
              <img src="/jacob-canner.webp" alt="Jacob Canner" class="w-full h-full object-cover transition-all duration-500 saturate-0 contrast-[1.1] group-hover:saturate-100 group-hover:contrast-100" />
            </div>
          </div>
          <div class="lg:col-span-8">
            <p class="text-xs tracking-widest uppercase text-gray-400 group-hover:text-white/50 font-medium mb-2 transition-colors duration-300">Founding Partner</p>
            <h2 class="text-2xl md:text-3xl lg:text-4xl font-light text-navy group-hover:text-white tracking-tight transition-colors duration-300 mb-2">
              Jacob Canner
            </h2>
            <p class="text-sm tracking-widest uppercase text-teal group-hover:text-white/70 font-medium mb-6 transition-colors duration-300">Distribution Networks & Logistics</p>
            <p class="text-base md:text-lg text-gray-500 group-hover:text-white/80 font-light leading-relaxed transition-colors duration-300 max-w-xl mb-4">
              Former operations director specializing in high-volume distribution and strategic partnerships. Built controlled distribution channels that expanded market reach for global brands.
            </p>
            <p class="text-base md:text-lg text-gray-500 group-hover:text-white/80 font-light leading-relaxed transition-colors duration-300 max-w-xl">
              Jacob scaled one of StockX's largest apparel pipelines from high school hustle. His volume distribution expertise and factory-level cost knowledge directly address the bloated intermediaries that drain brand margins and slow growth.
            </p>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- Our Approach -->
  <div class="py-20 md:py-28 bg-gray-50">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16">
        <div class="lg:col-span-4">
          <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Our Approach</p>
          <h2 class="text-3xl md:text-4xl font-light text-navy tracking-tight leading-tight">
            Operators, not consultants.
          </h2>
        </div>
        <div class="lg:col-span-8">
          <div class="space-y-6 text-gray-600 text-base md:text-lg font-light leading-relaxed">
            <p>
              We are not traditional consultants. We are operators who have built, scaled, and optimized operations at the world's most demanding companies.
            </p>
            <p>
              Every engagement is led by a partner—not a team of analysts fresh out of business school. We roll up our sleeves and work alongside your team on the factory floor, in the warehouse, and across your supply chain.
            </p>
            <p>
              Our fee structure reflects this philosophy. We don't bill by the hour. We price based on outcomes and share the risk of transformation with you.
            </p>
          </div>

          <!-- Highlight -->
          <div class="mt-12 p-8 md:p-10 bg-navy text-white">
            <p class="text-xl md:text-2xl font-light leading-relaxed">
              You get experienced operators, not PowerPoint presentations.
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
