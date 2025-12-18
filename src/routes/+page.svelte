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

<main class="pt-32 pb-20 px-5 md:px-10 font-sans text-black selection:bg-gray-200">
  
  <!-- Hero Headline -->
  <div class="mb-20 md:mb-32 max-w-5xl">
    <h1 class="text-4xl md:text-6xl lg:text-7xl leading-[1.1] font-normal tracking-tight">
      Manufacturing oversight and high-volume distribution for apparel brands who need predictable operations at scale.
    </h1>
  </div>

  <!-- Hero Carousel -->
  <div class="mb-32 relative -mx-5 md:-mx-10">
    <div bind:this={carousel} class="flex gap-4 md:gap-8 overflow-x-auto pb-8 snap-x snap-mandatory scrollbar-hide px-5 md:px-10">
      <!-- Left Image (Partial) -->
      <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-warehouse-distribution-center-with-organ-1765747100363-1.webp" alt="Distribution Operations" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
      
      <!-- Center Image (Main) -->
      <div class="shrink-0 w-[90vw] md:w-[70vw] lg:w-[50vw] snap-center relative">
        <img src="/generated/image-modern-apparel-factory-floor-with-worker-1765747098036-0.webp" alt="Factory Operations" class="w-full h-[400px] md:h-[600px] object-cover" />
        <div class="mt-4">
          <h3 class="text-lg font-medium">Direct Factory Oversight</h3>
          <p class="text-gray-500 text-lg">Eliminating cost inflation through hands-on production management</p>
        </div>
      </div>

      <!-- Right Image (Partial) -->
      <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-quality-inspector-examining-fabric-mater-1765747102486-2.webp" alt="Quality Control" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
       <!-- Extra Image -->
       <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-stacks-of-packaged-apparel-products-read-1765747104525-3.webp" alt="Fulfillment" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
    </div>
  </div>

  <!-- Services -->
  <Section label="Our Services">
    <div class="flex flex-col border-t border-gray-200">
      {#each services as service}
        <a href="/" class="py-6 border-b border-gray-200 text-3xl md:text-4xl lg:text-5xl font-normal hover:text-gray-500 transition-colors block">
          {service}
        </a>
      {/each}
    </div>
  </Section>

  <!-- Case Studies -->
  <Section label="Proven Results" link="/" linkText="View all case studies">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each caseStudies as item}
        <article class="group cursor-pointer">
          <div class="overflow-hidden mb-4">
            <img src={item.image} alt={item.title} class="w-full aspect-[4/3] object-cover group-hover:scale-105 transition-transform duration-500" />
          </div>
          <time class="text-gray-500 text-sm block mb-2">{item.date}</time>
          <h3 class="text-xl leading-snug group-hover:underline decoration-1 underline-offset-4">{item.title}</h3>
        </article>
      {/each}
    </div>
    
    <!-- Navigation Arrows -->
    <div class="flex justify-between mt-12 border-t border-transparent">
      <button class="hover:opacity-50 transition-opacity p-2 -ml-2">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M19 12H5M12 19l-7-7 7-7"/>
        </svg>
      </button>
      <button class="hover:opacity-50 transition-opacity p-2 -mr-2">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M5 12h14M12 5l7 7-7 7"/>
        </svg>
      </button>
    </div>
  </Section>

  <!-- Our Approach -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-10 md:gap-20 py-20 md:py-32">
    <div>
      <img src="/generated/image-business-partners-reviewing-production-d-1765747106701-4.webp" alt="Direct Partnership" class="w-full aspect-[4/3] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Manufacturing: Direct factory oversight</h3>
      <p class="text-gray-500 text-lg leading-relaxed">
        Built through years of hands-on sourcing experience, our factory networks eliminate intermediaries and cost inflation. We provide direct oversight of production lifecycles, ensuring quality control and preventing supply chain leaks that damage brand integrity.
      </p>
    </div>
    <div>
      <img src="/generated/image-global-shipping-containers-at-port-inter-1765747108784-5.webp" alt="Global Network" class="w-full aspect-[4/3] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Distribution: Distrint's proven channels</h3>
      <p class="text-gray-500 text-lg leading-relaxed">
        Our distribution arm moves product at scale through vetted marketplace channels. From ongoing partnerships to discreet liquidation, we provide flexible fulfillment backed by top-tier performance on StockX, eBay, Whatnot, and TikTok Shop.
      </p>
    </div>
  </div>

  <!-- Key Results -->
  <Section label="Track Record">
    <div class="flex flex-col gap-2">
      {#each results as result}
        <a href="/" class="group block">
          <h3 class="text-3xl md:text-5xl lg:text-6xl font-normal leading-tight">
            <span class="group-hover:underline decoration-1 underline-offset-8">{result.name}</span>
            {#if result.desc}
              <span class="text-gray-300 ml-2 group-hover:text-gray-400 transition-colors">{result.desc}</span>
            {/if}
          </h3>
        </a>
      {/each}
      
      <a href="/" class="inline-flex items-center gap-2 text-lg text-gray-500 mt-12 hover:text-black transition-colors group">
        → <span class="group-hover:translate-x-1 transition-transform">Learn more about our approach</span>
      </a>
    </div>
  </Section>

  <!-- Get in touch -->
  <div id="contact" class="py-20 md:py-32">
    <div class="max-w-xl">
      <img src="/generated/image-two-confident-business-founders-in-casua-1765747110893-6.webp" alt="Gabe Gorman and Jacob Canner" class="w-full aspect-[3/2] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Work with the founding partners</h3>
      <p class="text-gray-500 text-lg mb-6">
        Gabe Gorman built overseas factory networks through military discipline and large-scale sourcing. Jacob Canner scaled one of StockX's largest apparel pipelines and brings volume distribution expertise through Distrint. Together, they eliminate cost inflation and move product at scale.
      </p>
      <a href="mailto:contact@cgoperatinggroup.com" class="inline-flex items-center gap-2 px-6 py-3 border border-gray-200 hover:bg-black hover:text-white transition-colors text-sm font-medium">
        Get in Touch →
      </a>
    </div>
  </div>

  <!-- Footer -->
  <footer class="pt-20 border-t border-gray-200">
    <div class="grid grid-cols-1 md:grid-cols-12 gap-10 md:gap-4">
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
        <p class="text-sm text-gray-600 leading-relaxed">
          Predictable manufacturing and distribution for apparel brands.
        </p>
      </div>

      <!-- Links Columns -->
      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">Company</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="#contact" class="hover:text-black">Contact</a></li>
          <li><a href="/" class="hover:text-black">About</a></li>
          <li><a href="/" class="hover:text-black">Founders</a></li>
          <li><a href="/" class="hover:text-black">Case Studies</a></li>
          <li><a href="/" class="hover:text-black">Approach</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">Services</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">Manufacturing Oversight</a></li>
          <li><a href="/" class="hover:text-black">Factory Networks</a></li>
          <li><a href="/" class="hover:text-black">Cost Optimization</a></li>
          <li><a href="/" class="hover:text-black">Distribution (Distrint)</a></li>
          <li><a href="/" class="hover:text-black">Marketplace Fulfillment</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">Industries</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">Apparel Brands</a></li>
          <li><a href="/" class="hover:text-black">Footwear</a></li>
          <li><a href="/" class="hover:text-black">Accessories</a></li>
        </ul>
      </div>

      <!-- Contact -->
      <div class="col-span-1 md:col-span-3 flex flex-col justify-end">
        <div class="text-sm text-gray-600">
          <p class="mb-2 font-medium text-gray-800">Get in Touch</p>
          <a href="mailto:contact@cgoperatinggroup.com" class="hover:text-black block mb-1">contact@cgoperatinggroup.com</a>
        </div>
      </div>
    </div>

    <!-- Bottom Footer -->
    <div class="mt-20 py-8 flex flex-col md:flex-row justify-between items-start md:items-center text-xs text-gray-500 gap-4">
      <div>Copyright © 2025 CG Operating Group</div>

      <div class="flex gap-6">
        <a href="/" class="hover:text-black">Privacy Policy</a>
        <a href="/" class="hover:text-black">Terms of Service</a>
      </div>

      <div class="flex gap-6">
        <a href="/" class="hover:text-black">LinkedIn</a>
        <a href="/" class="hover:text-black">Twitter</a>
      </div>
    </div>
  </footer>

</main>

