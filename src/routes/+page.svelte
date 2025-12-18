<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import Section from "$lib/components/Section.svelte";

  const services = [
    { text: "Manufacturing: Direct factory oversight and quality control", type: "manufacturing" },
    { text: "Manufacturing: Global production networks and cost optimization", type: "manufacturing" },
    { text: "Distribution: High-volume marketplace operations", type: "distribution" },
    { text: "Distribution: Velocity liquidation at scale", type: "distribution" },
    { text: "Distribution: Strategic brand partnerships", type: "distribution" }
  ];

  const results = [
    { name: "100,000+ Units Monthly", desc: "Hat brand manufacturing with upgraded quality", type: "manufacturing" },
    { name: "Beat Cost & Improved Quality", desc: "Global athletic brand manufacturing", type: "manufacturing" },
    { name: "Top Seller on StockX", desc: "Distribution performance", type: "distribution" },
    { name: "Sub-60 Ranking TikTok Shop", desc: "Elite marketplace distribution", type: "distribution" },
    { name: "Thousands of Reviews on eBay", desc: "Proven seller reputation", type: "distribution" },
    { name: "Top-Tier Whatnot Performance", desc: "Live commerce excellence", type: "distribution" }
  ];

  // Carousel images - doubled for infinite scroll
  const carouselImages = [
    { src: '/warehouse.webp', alt: 'Distribution Operations', caption: 'Distribution', desc: '100,000+ units monthly' },
    { src: '/packaging.webp', alt: 'Quality Fulfillment', caption: 'Fulfillment', desc: 'Precision at every step' },
    { src: '/shipping.webp', alt: 'Global Shipping', caption: 'Logistics', desc: 'Global reach, local control' },
    { src: '/warehouse.webp', alt: 'Distribution Operations', caption: 'Distribution', desc: '100,000+ units monthly' },
    { src: '/packaging.webp', alt: 'Quality Fulfillment', caption: 'Fulfillment', desc: 'Precision at every step' },
    { src: '/shipping.webp', alt: 'Global Shipping', caption: 'Logistics', desc: 'Global reach, local control' },
  ];
</script>

<Header />

<main class="pt-36 pb-0 font-sans text-navy">

  <!-- Hero Headline -->
  <div class="px-6 md:px-16 lg:px-24 mb-12 md:mb-20 max-w-[1600px] mx-auto">
    <h1 class="text-4xl md:text-5xl lg:text-6xl leading-[1.1] font-light tracking-[-0.02em] text-gray-500 max-w-6xl">
      We are a <mark class="bg-navy/10 text-navy px-2 -mx-1">manufacturing</mark> and <mark class="bg-teal/15 text-teal px-2 -mx-1">distribution</mark> infrastructure company, built for brands that need scale without sacrifice.
    </h1>
    <p class="mt-6 text-lg md:text-xl text-gray-400 font-light max-w-2xl">
      Global manufacturing and large-scale distribution.<br />
      Built for brands that need precision and reach.
    </p>
    <a href="/contact" class="inline-block mt-8 px-8 py-4 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150">
      Get in Touch
    </a>
  </div>

  <!-- Hero Carousel -->
  <div class="relative overflow-hidden mb-16 md:mb-24">
    <!-- Edge fades -->
    <div class="absolute left-0 top-0 bottom-0 w-16 md:w-32 bg-gradient-to-r from-white/60 to-transparent z-10 pointer-events-none"></div>
    <div class="absolute right-0 top-0 bottom-0 w-16 md:w-32 bg-gradient-to-l from-white/60 to-transparent z-10 pointer-events-none"></div>

    <div class="carousel-track flex gap-4 md:gap-6">
      {#each carouselImages as image, i}
        <div class="carousel-item shrink-0 cursor-pointer relative overflow-hidden">
          <img
            src={image.src}
            alt={image.alt}
            class="w-[400px] md:w-[550px] lg:w-[700px] h-[300px] md:h-[420px] lg:h-[520px] object-cover"
          />
          <div class="carousel-caption absolute bottom-0 left-0 right-0 p-5 md:p-8 bg-gradient-to-t from-black/80 to-transparent">
            <p class="text-white text-lg md:text-xl font-medium">{image.caption}</p>
            <p class="text-white/70 text-sm md:text-base">{image.desc}</p>
          </div>
        </div>
      {/each}
    </div>
  </div>

  <!-- Intro Text -->
  <div class="py-20 md:py-32 border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-16">
      <div class="lg:col-span-3">
        <p class="text-xs tracking-widest uppercase text-gray-400 font-medium">The Problem</p>
      </div>
      <div class="lg:col-span-9">
        <p class="text-2xl md:text-3xl lg:text-4xl text-gray-500 font-light leading-[1.3] tracking-tight max-w-4xl">
          Supply chains fail when brands are forced to manage inefficiencies instead of growth. We provide two capabilities: <mark class="bg-navy/10 text-navy px-1.5 -mx-0.5">manufacturing</mark> and <mark class="bg-teal/15 text-teal px-1.5 -mx-0.5">distribution</mark>.
        </p>
        <div class="mt-10 grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl">
          <div>
            <p class="text-sm tracking-widest uppercase text-navy font-medium mb-3">Manufacturing</p>
            <p class="text-gray-500 font-light leading-relaxed">Disciplined production with direct factory oversight. We eliminate cost inflation and quality gaps at the source.</p>
          </div>
          <div>
            <p class="text-sm tracking-widest uppercase text-teal font-medium mb-3">Distribution</p>
            <p class="text-gray-500 font-light leading-relaxed">High-volume movement through strategic channels. We expand reach without undercutting your core retail strategy.</p>
          </div>
        </div>
      </div>
      </div>
    </div>
  </div>

  <!-- Stats Strip -->
  <div class="px-6 md:px-16 lg:px-24 py-16 md:py-20 bg-gray-50">
    <div class="grid grid-cols-2 md:grid-cols-4 gap-8 md:gap-12 text-center max-w-[1600px] mx-auto">
      <div>
        <p class="text-4xl md:text-5xl lg:text-6xl font-light text-navy tracking-tight">100K+</p>
        <p class="text-sm text-gray-500 mt-2 font-light">Units monthly</p>
      </div>
      <div>
        <p class="text-4xl md:text-5xl lg:text-6xl font-light text-teal tracking-tight">#1</p>
        <p class="text-sm text-gray-500 mt-2 font-light">StockX seller ranking</p>
      </div>
      <div>
        <p class="text-4xl md:text-5xl lg:text-6xl font-light text-navy tracking-tight">40%</p>
        <p class="text-sm text-gray-500 mt-2 font-light">Cost reduction avg.</p>
      </div>
      <div>
        <p class="text-4xl md:text-5xl lg:text-6xl font-light text-teal tracking-tight">6+</p>
        <p class="text-sm text-gray-500 mt-2 font-light">Distribution channels</p>
      </div>
    </div>
  </div>

  <!-- Page Navigation -->
  <div class="py-16 md:py-24">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6">
      <a href="/needs" class="group block bg-navy p-8 md:p-12 hover:bg-navy-600 transition-colors duration-200">
        <p class="text-white/50 text-xs tracking-widest uppercase font-medium mb-6">01</p>
        <h3 class="text-3xl md:text-4xl font-light text-white tracking-tight mb-4">Your Needs</h3>
        <p class="text-white/60 font-light mb-8">Manufacturing or distribution — we deliver the infrastructure.</p>
        <span class="text-white text-sm font-medium inline-flex items-center gap-2 group-hover:gap-3 transition-all duration-200">
          Explore <span>→</span>
        </span>
      </a>
      <a href="/impact" class="group block bg-teal p-8 md:p-12 hover:bg-teal-500 transition-colors duration-200">
        <p class="text-white/60 text-xs tracking-widest uppercase font-medium mb-6">02</p>
        <h3 class="text-3xl md:text-4xl font-light text-white tracking-tight mb-4">Our Impact</h3>
        <p class="text-white/60 font-light mb-8">Real results. Measurable. 100K+ units moved monthly.</p>
        <span class="text-white text-sm font-medium inline-flex items-center gap-2 group-hover:gap-3 transition-all duration-200">
          Explore <span>→</span>
        </span>
      </a>
      <a href="/firm" class="group block bg-gray-100 p-8 md:p-12 hover:bg-gray-200 transition-colors duration-200 md:col-span-2 lg:col-span-1">
        <p class="text-gray-400 text-xs tracking-widest uppercase font-medium mb-6">03</p>
        <h3 class="text-3xl md:text-4xl font-light text-navy tracking-tight mb-4">The Firm</h3>
        <p class="text-gray-500 font-light mb-8">Meet the partners behind the operation.</p>
        <span class="text-navy text-sm font-medium inline-flex items-center gap-2 group-hover:gap-3 transition-all duration-200">
          Explore <span>→</span>
        </span>
      </a>
      </div>
    </div>
  </div>

  <!-- Capabilities -->
  <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
    <Section label="Capabilities">
      <div class="flex flex-col">
        {#each services as service, i}
          <a
            href="/"
            class={[
              'py-6 md:py-8 -mx-6 px-6 text-2xl md:text-4xl lg:text-5xl font-light tracking-tight transition-all duration-300 block group',
              service.type === 'manufacturing'
                ? 'hover:bg-navy hover:text-white'
                : 'hover:bg-teal hover:text-white'
            ]}
          >
            <span class="inline-block group-hover:translate-x-4 transition-transform duration-300">{service.text}</span>
          </a>
        {/each}
      </div>
    </Section>
  </div>

  <!-- Who We Are -->
  <div class="py-20 md:py-32">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">
      <!-- Text -->
      <div class="lg:col-span-5">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy mb-10 tracking-tight leading-tight">
          Who We Are
        </h2>
        <div class="space-y-6 text-gray-600 text-lg md:text-xl font-light leading-relaxed">
          <p>
            CG Operating Group was founded in 2025 after watching supply chains collapse under basic pressure. Our first arm rebuilds broken supply chains from the ground up. We compete on pricing, timelines, quality, and leak-prevention, giving companies a level of operational control they've never had. Every step becomes predictable, measurable, and actually aligned with the brand's goals.
          </p>
          <p>
            Our second arm is a high-volume distribution network built for brands that need more reach. We partner with companies to move products through controlled, strategic channels that increase exposure without undercutting their core retail strategy. It's not liquidation. It's a structured distribution that expands visibility and gets products into the market at scale.
          </p>
        </div>
      </div>

      <!-- Image -->
      <div class="lg:col-span-7">
        <img src="/partners.webp" alt="CG Operating Group Partners" class="w-full aspect-[4/3] object-cover" />
      </div>
      </div>
    </div>
  </div>

  <!-- Impact / Results -->
  <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
    <Section label="Our Impact">
      <div class="flex flex-col">
        {#each results as result}
          <a
            href="/"
            class={[
              'group block py-5 md:py-6 -mx-6 px-6 transition-all duration-300',
              result.type === 'manufacturing'
                ? 'hover:bg-navy hover:text-white'
                : 'hover:bg-teal hover:text-white'
            ]}
          >
            <h3 class={[
              'text-2xl md:text-4xl lg:text-5xl font-light leading-tight tracking-tight transition-colors duration-300',
              result.type === 'manufacturing' ? 'text-navy group-hover:text-white' : 'text-teal group-hover:text-white'
            ]}>
              <span class="group-hover:translate-x-4 inline-block transition-transform duration-300">{result.name}</span>
            </h3>
            {#if result.desc}
              <p class="text-gray-500 text-base md:text-lg mt-2 font-light group-hover:text-white/70 transition-colors duration-300">{result.desc}</p>
            {/if}
          </a>
        {/each}
      </div>
    </Section>
  </div>

  <!-- The Firm / Leadership -->
  <div class="px-6 md:px-16 lg:px-24 py-20 md:py-32 max-w-[1600px] mx-auto">
    <Section label="The Firm">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-16 md:gap-24">
        <div>
          <img src="/gabe-gorman.webp" alt="Gabe Gorman" class="w-full aspect-[4/3] object-cover mb-8 bg-gray-100" />
          <h3 class="text-2xl md:text-3xl font-light text-navy mb-2 tracking-tight">Gabe Gorman</h3>
          <p class="text-teal text-sm tracking-widest uppercase font-medium mb-4">Founding Partner</p>
          <p class="text-gray-600 text-base md:text-lg leading-relaxed font-light">
            Gabe built overseas factory networks through military discipline and large-scale sneaker sourcing. His hands-on supply chain experience eliminates the cost inflation and logistical chaos brands face when scaling manufacturing operations globally.
          </p>
        </div>
        <div>
          <img src="/jacob-canner.webp" alt="Jacob Canner" class="w-full aspect-[4/3] object-cover mb-8 bg-gray-100" />
          <h3 class="text-2xl md:text-3xl font-light text-navy mb-2 tracking-tight">Jacob Canner</h3>
          <p class="text-teal text-sm tracking-widest uppercase font-medium mb-4">Founding Partner</p>
          <p class="text-gray-600 text-base md:text-lg leading-relaxed font-light">
            Jacob scaled one of StockX's largest apparel pipelines from high school hustle. His volume distribution expertise and factory-level cost knowledge directly address the bloated intermediaries that drain brand margins and slow growth.
          </p>
        </div>
      </div>
    </Section>
  </div>

  <!-- CTA -->
  <div class="py-24 md:py-32 border-t border-gray-100">
    <div class="px-6 md:px-16 lg:px-24 max-w-[1600px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-20">
      <div class="lg:col-span-7">
        <p class="text-xs tracking-widest uppercase text-gray-400 font-medium mb-6">Work With Us</p>
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-light text-navy leading-tight tracking-tight max-w-2xl">
          Ready to scale without the operational burden?
        </h2>
      </div>
      <div class="lg:col-span-5 flex flex-col justify-end">
        <p class="text-gray-500 font-light text-lg leading-relaxed mb-8">
          Whether you need manufacturing oversight or distribution reach, we're ready to discuss how we can support your growth.
        </p>
        <div class="flex flex-col sm:flex-row gap-4">
          <a href="/contact" class="px-8 py-4 bg-navy text-white text-sm font-medium tracking-wide hover:bg-navy-600 transition-colors duration-150 text-center">
            Start a Conversation
          </a>
          <a href="/firm" class="px-8 py-4 border border-gray-300 text-navy text-sm font-medium tracking-wide hover:border-navy hover:bg-navy hover:text-white transition-all duration-150 text-center">
            Learn About Us
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

<style>
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%);
    }
  }

  .carousel-track {
    animation: scroll 25s linear infinite;
    width: max-content;
  }

  .carousel-track:hover {
    animation-play-state: paused;
  }

  .carousel-item {
    transition: transform 0.15s ease-out, opacity 0.15s ease-out;
  }

  .carousel-item:hover {
    transform: scale(1.02);
  }

  .carousel-track:hover .carousel-item:not(:hover) {
    opacity: 0.6;
  }

  .carousel-caption {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.15s ease-out, transform 0.15s ease-out;
  }

  .carousel-item:hover .carousel-caption {
    opacity: 1;
    transform: translateY(0);
  }
</style>
