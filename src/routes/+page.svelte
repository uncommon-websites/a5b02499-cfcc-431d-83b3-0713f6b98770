<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import Section from "$lib/components/Section.svelte";
  
  const services = [
    "Manufacturing: Direct factory oversight and quality control",
    "Manufacturing: Global production networks and cost optimization",
    "Distribution: High-volume marketplace operations (Distrint)",
    "Distribution: Liquidation and inventory management",
    "Distribution: Multi-channel fulfillment and logistics"
  ];

  const caseStudies = [
    {
      date: "Manufacturing",
      title: "Hat brand: Removed supply-chain leakages and upgraded quality while moving 100,000+ units monthly",
      image: "/generated/image-stacks-of-packaged-apparel-products-read-1765747104525-3.webp"
    },
    {
      date: "Manufacturing",
      title: "Global athletic brand: Beat cost and improved quality while expanding multi-country distribution",
      image: "/generated/image-modern-apparel-factory-floor-with-worker-1765747098036-0.webp"
    },
    {
      date: "Distribution (Distrint)",
      title: "Scaled to top seller on StockX, sub-60 on TikTok Shop, thousands of reviews on eBay, top-tier on Whatnot",
      image: "/generated/image-warehouse-distribution-center-with-organ-1765747100363-1.webp"
    }
  ];

  const results = [
    { name: "100,000+ Units Monthly", desc: "Hat brand manufacturing with upgraded quality", highlight: true },
    { name: "Beat Cost & Improved Quality", desc: "Global athletic brand manufacturing", highlight: true },
    { name: "Top Seller on StockX", desc: "Distrint distribution performance", highlight: true },
    { name: "Sub-60 Ranking TikTok Shop", desc: "Elite marketplace distribution", highlight: false },
    { name: "Thousands of Reviews on eBay", desc: "Proven Distrint seller reputation", highlight: false },
    { name: "Top-Tier Whatnot Performance", desc: "Live commerce distribution excellence", highlight: false },
    { name: "Direct Factory Networks", desc: "Built through hands-on sourcing experience", highlight: false },
    { name: "Multi-Country Distribution", desc: "Expanded for global athletic brand", highlight: false },
    { name: "Supply Chain Leak Prevention", desc: "Controlled production oversight", highlight: true }
  ];
  let carousel: HTMLElement;

  import { onMount } from 'svelte';
  
  onMount(() => {
    if (carousel) {
      const centerImage = carousel.children[1] as HTMLElement;
      if (centerImage) {
        const scrollLeft = centerImage.offsetLeft - (carousel.clientWidth - centerImage.clientWidth) / 2;
        carousel.scrollLeft = scrollLeft;
      }
    }
  });
</script>

<Header />

<main class="pt-40 pb-32 px-6 md:px-16 lg:px-24 font-sans text-black selection:bg-gray-200">
  
  <!-- Hero Headline -->
  <div class="mb-32 md:mb-48 max-w-7xl">
    <h1 class="text-5xl md:text-7xl lg:text-8xl leading-[1.05] font-light tracking-[-0.02em] text-gray-900">
      The system that works so you don't have to.
    </h1>
    <p class="text-xl md:text-2xl text-gray-500 mt-8 max-w-3xl font-light leading-relaxed">
      Predictable operations. Direct factory networks. Proven marketplace performance.
    </p>
  </div>

  <!-- Hero Carousel -->
  <div class="mb-48 relative -mx-6 md:-mx-16 lg:-mx-24">
    <div bind:this={carousel} class="flex gap-6 md:gap-12 overflow-x-auto pb-12 snap-x snap-mandatory scrollbar-hide px-6 md:px-16 lg:px-24">
      <!-- Left Image (Partial) -->
      <div class="shrink-0 w-[85vw] md:w-[65vw] lg:w-[45vw] snap-center opacity-40 grayscale transition-all duration-700 hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-warehouse-distribution-center-with-organ-1765747100363-1.webp" alt="Distribution Operations" class="w-full h-[450px] md:h-[650px] object-cover" />
      </div>
      
      <!-- Center Image (Main) -->
      <div class="shrink-0 w-[90vw] md:w-[75vw] lg:w-[55vw] snap-center relative">
        <img src="/generated/image-modern-apparel-factory-floor-with-worker-1765747098036-0.webp" alt="Factory Operations" class="w-full h-[450px] md:h-[650px] object-cover" />
        <div class="mt-8">
          <h3 class="text-xl md:text-2xl font-light text-gray-900 tracking-tight">Direct Factory Oversight</h3>
          <p class="text-gray-500 text-lg md:text-xl mt-2 font-light">Eliminating cost inflation through hands-on production management</p>
        </div>
      </div>

      <!-- Right Image (Partial) -->
      <div class="shrink-0 w-[85vw] md:w-[65vw] lg:w-[45vw] snap-center opacity-40 grayscale transition-all duration-700 hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-quality-inspector-examining-fabric-mater-1765747102486-2.webp" alt="Quality Control" class="w-full h-[450px] md:h-[650px] object-cover" />
      </div>
       <!-- Extra Image -->
       <div class="shrink-0 w-[85vw] md:w-[65vw] lg:w-[45vw] snap-center opacity-40 grayscale transition-all duration-700 hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-stacks-of-packaged-apparel-products-read-1765747104525-3.webp" alt="Fulfillment" class="w-full h-[450px] md:h-[650px] object-cover" />
      </div>
    </div>
  </div>

  <!-- Services -->
  <Section label="Capabilities">
    <div class="flex flex-col">
      {#each services as service, i}
        <a href="/" class={[
          'py-8 md:py-10 border-b border-gray-100 text-3xl md:text-5xl lg:text-6xl font-light tracking-tight transition-all duration-500 block group',
          service.startsWith('Manufacturing') ? 'hover:text-blue-700 hover:translate-x-2' : 'hover:text-slate-800 hover:translate-x-2'
        ]}>
          <span class="inline-block transition-transform duration-500">{service}</span>
        </a>
      {/each}
    </div>
  </Section>

  <!-- Case Studies -->
  <Section label="Case Studies" link="/" linkText="View all">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12 md:gap-16">
      {#each caseStudies as item}
        <article class="group cursor-pointer">
          <div class="overflow-hidden mb-6 bg-gray-50">
            <img src={item.image} alt={item.title} class="w-full aspect-[4/3] object-cover group-hover:scale-[1.02] transition-transform duration-700" />
          </div>
          <time class={[
            'text-xs block mb-3 font-medium tracking-wider uppercase',
            item.date.includes('Manufacturing') ? 'text-blue-700' : 'text-slate-700'
          ]}>{item.date}</time>
          <h3 class="text-xl md:text-2xl leading-snug font-light text-gray-900 group-hover:text-blue-700 transition-colors duration-300">{item.title}</h3>
        </article>
      {/each}
    </div>
  </Section>

  <!-- Marketplace Trust Signals -->
  <Section label="Distribution Network">
    <div class="bg-slate-50 border border-slate-100 p-12 md:p-16">
      <h3 class="text-3xl md:text-4xl font-light mb-12 text-gray-900 tracking-tight">Enterprise-grade marketplace performance</h3>
      <div class="grid grid-cols-2 md:grid-cols-4 gap-12 mb-12">
        <div class="flex flex-col items-center text-center">
          <div class="w-20 h-20 bg-white border border-slate-200 flex items-center justify-center mb-4 transition-all duration-300 hover:border-slate-400">
            <span class="text-2xl font-medium text-slate-800">SX</span>
          </div>
          <p class="text-sm font-medium text-gray-900">StockX</p>
          <p class="text-xs text-gray-500 mt-2 font-light">Top Seller</p>
        </div>
        <div class="flex flex-col items-center text-center">
          <div class="w-20 h-20 bg-white border border-slate-200 flex items-center justify-center mb-4 transition-all duration-300 hover:border-slate-400">
            <span class="text-2xl font-medium text-slate-800">EB</span>
          </div>
          <p class="text-sm font-medium text-gray-900">eBay</p>
          <p class="text-xs text-gray-500 mt-2 font-light">Thousands of Reviews</p>
        </div>
        <div class="flex flex-col items-center text-center">
          <div class="w-20 h-20 bg-white border border-slate-200 flex items-center justify-center mb-4 transition-all duration-300 hover:border-slate-400">
            <span class="text-2xl font-medium text-slate-800">TT</span>
          </div>
          <p class="text-sm font-medium text-gray-900">TikTok Shop</p>
          <p class="text-xs text-gray-500 mt-2 font-light">Sub-60 Ranking</p>
        </div>
        <div class="flex flex-col items-center text-center">
          <div class="w-20 h-20 bg-white border border-slate-200 flex items-center justify-center mb-4 transition-all duration-300 hover:border-slate-400">
            <span class="text-2xl font-medium text-slate-800">WN</span>
          </div>
          <p class="text-sm font-medium text-gray-900">Whatnot</p>
          <p class="text-xs text-gray-500 mt-2 font-light">Top-Tier Performance</p>
        </div>
      </div>
      <p class="text-gray-600 text-lg md:text-xl font-light leading-relaxed max-w-4xl">
        Distrint delivers proven high-volume fulfillment across the industry's most demanding platforms, providing vetted channels for ongoing partnerships and discreet liquidation at scale.
      </p>
    </div>
  </Section>

  <!-- Our Approach -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-16 md:gap-24 py-32 md:py-48">
    <div class="border-l border-slate-200 pl-10">
      <img src="/generated/image-business-partners-reviewing-production-d-1765747106701-4.webp" alt="Direct Partnership" class="w-full aspect-[4/3] object-cover mb-8 bg-gray-50" />
      <h3 class="text-2xl md:text-3xl font-light mb-4 text-blue-700 tracking-tight">Manufacturing oversight</h3>
      <p class="text-gray-600 text-lg md:text-xl leading-relaxed font-light">
        Direct factory networks built through years of hands-on sourcing eliminate intermediaries and cost inflation. We provide comprehensive oversight of production lifecycles, ensuring quality control and preventing supply chain leaks.
      </p>
    </div>
    <div class="border-l border-slate-200 pl-10">
      <img src="/generated/image-global-shipping-containers-at-port-inter-1765747108784-5.webp" alt="Global Network" class="w-full aspect-[4/3] object-cover mb-8 bg-gray-50" />
      <h3 class="text-2xl md:text-3xl font-light mb-4 text-slate-800 tracking-tight">High-volume distribution</h3>
      <p class="text-gray-600 text-lg md:text-xl leading-relaxed font-light">
        Distrint moves product at scale through vetted marketplace channels with proven performance. From ongoing partnerships to discreet liquidation, we deliver flexible fulfillment backed by top-tier marketplace rankings.
      </p>
    </div>
  </div>

  <!-- Key Results -->
  <Section label="Performance Metrics">
    <div class="flex flex-col gap-6">
      {#each results as result}
        <a href="/" class="group block py-4 border-b border-slate-100 hover:border-slate-300 transition-all duration-300">
          <h3 class="text-3xl md:text-5xl lg:text-6xl font-light leading-tight tracking-tight">
            <span class={[
              'transition-colors duration-300',
              result.highlight ? 'text-blue-700 group-hover:text-blue-800' : 'text-gray-900 group-hover:text-blue-700'
            ]}>{result.name}</span>
            {#if result.desc}
              <span class="text-gray-300 ml-3 text-2xl md:text-3xl lg:text-4xl group-hover:text-gray-400 transition-colors duration-300 font-extralight">{result.desc}</span>
            {/if}
          </h3>
        </a>
      {/each}
      
      <a href="/" class="inline-flex items-center gap-3 text-lg md:text-xl text-gray-500 mt-16 hover:text-blue-700 transition-colors duration-300 group font-light">
        <span class="group-hover:translate-x-2 transition-transform duration-300">Learn more about our approach</span>
        <span class="text-2xl">→</span>
      </a>
    </div>
  </Section>

  <!-- Get in touch -->
  <div id="contact" class="py-32 md:py-48">
    <div class="max-w-2xl">
      <img src="/generated/image-two-confident-business-founders-in-casua-1765747110893-6.webp" alt="Gabe Gorman and Jacob Canner" class="w-full aspect-[3/2] object-cover mb-8 bg-gray-50" />
      <div class="flex gap-3 mb-6">
        <span class="px-4 py-2 bg-slate-100 text-slate-700 text-xs font-medium tracking-wider uppercase">Military Discipline</span>
        <span class="px-4 py-2 bg-slate-100 text-slate-700 text-xs font-medium tracking-wider uppercase">StockX Top Seller</span>
        <span class="px-4 py-2 bg-slate-100 text-slate-700 text-xs font-medium tracking-wider uppercase">Factory Networks</span>
      </div>
      <h3 class="text-2xl md:text-3xl font-light mb-6 text-gray-900 tracking-tight">Leadership</h3>
      <p class="text-gray-600 text-lg md:text-xl mb-10 font-light leading-relaxed">
        <strong class="text-blue-700 font-normal">Gabe Gorman</strong> built overseas factory networks through military discipline and large-scale sourcing. <strong class="text-slate-800 font-normal">Jacob Canner</strong> scaled one of StockX's largest apparel pipelines and brings volume distribution expertise through Distrint. Together, they eliminate cost inflation and move product at scale.
      </p>
      <a href="mailto:contact@cgoperatinggroup.com" class="inline-flex items-center gap-3 px-8 py-4 bg-blue-700 text-white hover:bg-blue-800 transition-all duration-300 text-base font-normal tracking-wide hover:gap-4">
        Get in Touch
        <span class="text-xl">→</span>
      </a>
    </div>
  </div>

  <!-- Footer -->
  <footer class="pt-32 border-t border-slate-100">
    <div class="grid grid-cols-1 md:grid-cols-12 gap-16 md:gap-8">
      <!-- Logo Column -->
      <div class="col-span-1 md:col-span-3">
        <svg class="w-12 h-12 mb-4" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M5.0473 17.8386L5.69453 18.9586V18.9601H18.3003L18.9314 17.84H6.34063L6.82626 16.9993H19.4308L20.078 15.8807H7.47237L7.95715 15.0414H16.0358L16.0366 15.0429L16.0375 15.0414H20.5603L20.5612 15.0429L21.2084 13.9228L21.208 13.922L21.2084 13.9213H21.2075L14.9084 3.00677L14.9106 3.00296L14.9062 3.00296L13.6177 3.00296L5.0473 17.8386ZM14.261 4.12767L13.7751 4.96887L18.9438 13.9213H19.9139L14.261 4.12767ZM13.1286 6.08808L12.6467 6.9225L16.6749 13.9006L16.6634 13.9213H17.6511L13.1286 6.08808ZM11.9999 8.04225L8.60411 13.9213H15.3899L11.9999 8.04225ZM6.99833 3.30006C7.33866 3.10343 7.7248 2.99993 8.11786 3L2.30033 13.0776C2.10357 12.7371 2 12.3508 2 11.9575C2 11.5643 2.10357 11.178 2.30033 10.8375L6.17916 4.12006C6.37543 3.77951 6.65798 3.49669 6.99833 3.30006ZM9.08869 3H10.3816L3.43223 15.0384L2.785 13.9184L9.08869 3ZM11.3509 3H12.6424L4.56262 16.9963L3.91691 15.8777L11.3509 3ZM21.7064 13.0598C21.8988 12.7254 22 12.3463 22 11.9605C22 11.5746 21.8988 11.1956 21.7064 10.8611L17.8039 4.10233C17.6108 3.7681 17.3331 3.49057 16.9987 3.2976C16.6644 3.10463 16.2852 3.00302 15.8992 3.00296H15.8741L21.6931 13.082L21.7064 13.0598ZM17.7995 19.7994H6.17916C6.37472 20.1412 6.65692 20.4253 6.99728 20.6232C7.33763 20.8212 7.72414 20.9258 8.11786 20.9269H15.8829C16.2737 20.9261 16.6572 20.8212 16.994 20.6231C17.3309 20.4249 17.6089 20.1406 17.7995 19.7994Z"
            fill="currentColor"
          />
        </svg>
        <p class="text-sm text-gray-500 leading-relaxed font-light">
          Predictable manufacturing and distribution for apparel brands operating at scale.
        </p>
      </div>

      <!-- Links Columns -->
      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-8 text-xs tracking-wider uppercase font-medium">Company</h4>
        <ul class="space-y-3 text-sm text-gray-600 font-light">
          <li><a href="#contact" class="hover:text-blue-700 transition-colors duration-300">Contact</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">About</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Founders</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Case Studies</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Approach</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-8 text-xs tracking-wider uppercase font-medium">Services</h4>
        <ul class="space-y-3 text-sm text-gray-600 font-light">
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Manufacturing Oversight</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Factory Networks</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Cost Optimization</a></li>
          <li><a href="/" class="hover:text-slate-800 transition-colors duration-300">Distribution (Distrint)</a></li>
          <li><a href="/" class="hover:text-slate-800 transition-colors duration-300">Marketplace Fulfillment</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-8 text-xs tracking-wider uppercase font-medium">Industries</h4>
        <ul class="space-y-3 text-sm text-gray-600 font-light">
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Apparel Brands</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Footwear</a></li>
          <li><a href="/" class="hover:text-blue-700 transition-colors duration-300">Accessories</a></li>
        </ul>
      </div>

      <!-- Contact -->
      <div class="col-span-1 md:col-span-3 flex flex-col justify-end">
        <div class="text-sm text-gray-600">
          <p class="mb-3 font-normal text-gray-900">Get in Touch</p>
          <a href="mailto:contact@cgoperatinggroup.com" class="hover:text-blue-700 transition-colors duration-300 block mb-1 font-light">contact@cgoperatinggroup.com</a>
        </div>
      </div>
    </div>

    <!-- Bottom Footer -->
    <div class="mt-32 pt-12 border-t border-slate-100 flex flex-col md:flex-row justify-between items-start md:items-center text-xs text-gray-400 gap-6 font-light">
      <div>Copyright © 2025 CG Operating Group</div>

      <div class="flex gap-8">
        <a href="/" class="hover:text-blue-700 transition-colors duration-300">Privacy Policy</a>
        <a href="/" class="hover:text-blue-700 transition-colors duration-300">Terms of Service</a>
      </div>

      <div class="flex gap-8">
        <a href="/" class="hover:text-blue-700 transition-colors duration-300">LinkedIn</a>
        <a href="/" class="hover:text-blue-700 transition-colors duration-300">Twitter</a>
      </div>
    </div>
  </footer>

</main>

