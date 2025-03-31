<script>
  import { page } from '$app/stores';
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Skeleton } from 'flowbite-svelte';
  $: activeUrl = $page.url.pathname;

  let hoverStates = {
    '/': false,
    '/about': false,
    '/partners': false,
    '/careers': false,
    '/store': false
  };

  // @ts-ignore
  function getLinkStyle(href) {
    const isActive = activeUrl === href;
    // @ts-ignore
    const isHovered = hoverStates[href];
    return `color: ${isHovered ? '#109bd4' : (isActive ? '#109bd4' : '#ffffff')}`;
  }
</script>

<Navbar class="sticky top-0 z-50 shadow-md" style="background-color: #4b7163;">
  <NavBrand href="/">
    <img src="/main-logo.png" class="h-10 mr-3" alt="ClearCyle logo" />
    <span class="self-center text-4xl font-semibold whitespace-nowrap" style="color: #9ed4c3;">ClearCyle</span>
  </NavBrand>
  <NavHamburger />
  <NavUl activeUrl={activeUrl} class="md:flex md:items-center md:space-x-6">
    <NavLi
      href="/"
      class="text-xl"
      style={getLinkStyle('/')}
      on:mouseover={() => hoverStates['/'] = true}
      on:mouseleave={() => hoverStates['/'] = false}
    >
      Home
    </NavLi>
    <NavLi
      href="/about"
      class="text-xl"
      style={getLinkStyle('/about')}
      on:mouseover={() => hoverStates['/about'] = true}
      on:mouseleave={() => hoverStates['/about'] = false}
    >
      About Us
    </NavLi>
    <NavLi
      href="/partners"
      class="text-xl"
      style={getLinkStyle('/partners')}
      on:mouseover={() => hoverStates['/partners'] = true}
      on:mouseleave={() => hoverStates['/partners'] = false}
    >
      Partners
    </NavLi>
    <NavLi
      href="/careers"
      class="text-xl"
      style={getLinkStyle('/careers')}
      on:mouseover={() => hoverStates['/careers'] = true}
      on:mouseleave={() => hoverStates['/careers'] = false}
    >
      Careers
    </NavLi>
    <NavLi
      href="/store"
      class="text-xl"
      style={getLinkStyle('/store')}
      on:mouseover={() => hoverStates['/store'] = true}
      on:mouseleave={() => hoverStates['/store'] = false}
    >
      Store
    </NavLi>
  </NavUl>
</Navbar>

<!-- <Navbar class="sticky top-0 z-50 shadow-md" style="background-color: #4b7163;">
  <NavBrand href="/">
    <img src="/clear-cycle-logo.png" class="h-10 mr-3" alt="ClearCyle logo" />
    <span class="self-center text-4xl font-semibold whitespace-nowrap" style="color: #9ed4c3;">ClearCyle</span>
  </NavBrand>
  <NavHamburger />
  <NavUl activeUrl={activeUrl} class="md:flex md:items-center md:space-x-6">
    <NavLi href="/" class="text-xl" style={activeUrl === "/" ? 'color: #109bd4;' : 'color: #ffffff;'}>Home</NavLi>
    <NavLi href="/about" class="text-xl" style={activeUrl === "/about" ? 'color: #109bd4;' : 'color: #ffffff;'}>About Us</NavLi>
    <NavLi href="/partners" class="text-xl" style={activeUrl === "/partners" ? 'color: #109bd4;' : 'color: #ffffff;'}>Partners</NavLi>
    <NavLi href="/careers" class="text-xl" style={activeUrl === "/careers" ? 'color: #109bd4;' : 'color: #ffffff;'}>Careers</NavLi>
    <NavLi href="/store" class="text-xl" style={activeUrl === "/store" ? 'color: #109bd4;' : 'color: #ffffff;'}>Store</NavLi>
  </NavUl>
</Navbar> -->

<main class="overflow-y-auto">
  <section class="min-h-[calc(100vh-4rem)] flex flex-col md:flex-row items-center justify-center bg-gray-100">
    <div class="w-full md:w-1/2 h-full flex items-center justify-center">
      <img
        src="/hero.png"
        alt="Two people smiling, one handing a box with ClearCycle logo"
        class="object-cover h-full w-full md:w-auto"
      />
    </div>
    <div class="w-full md:w-1/2 p-8 text-center md:text-left">
      <h1 class="text-4xl font-bold text-gray-900 mb-4">
        Turn Clutter into Opportunity
      </h1>
      <p class="text-lg text-gray-700 mb-6">
        We’re ClearCycle—your hassle-free way to sell or donate the stuff you don’t need. From old gadgets to forgotten furniture, we make letting go feel good. Ready to declutter your life and spark someone else’s joy? Let’s make it happen—your junk’s next journey starts here!
      </p>
      <a
        href="/start"
        class="inline-block bg-blue-600 text-white font-semibold py-3 px-6 rounded-lg hover:bg-blue-700 transition"
      >
        Clear It Now
      </a>
    </div>
  </section>

  <section class="min-h-[calc(100vh-4rem)] flex flex-col md:flex-row items-center justify-center bg-white">
    <div class="w-full md:w-1/2 p-8">
      <h1 class="text-4xl font-bold text-gray-900 mb-4">
        Industry Leading Logistics
      </h1>
      <p class="text-lg text-gray-700 mb-6">
        From lightning-fast pickups to seamless deliveries, we’ve mastered the art of moving your unwanted stuff—whether it’s sold, donated, or repurposed. Our industry-leading network ensures your junk finds its next home without you lifting a finger.
      </p>
      <!-- <Skeleton class="h-4 w-3/4 mb-2" /> -->
      <!-- <Skeleton class="h-4 w-full mb-2" /> #4b7163 -->
      <!-- <Skeleton class="h-4 w-full mb-2" /> #4b7163 -->
      <!-- <Skeleton class="h-4 w-5/6 mb-2" /> #9ed4c3 -->
      <!-- <Skeleton class="h-4 w-2/3" /> #efefef -->
    </div>
    <div class="w-full md:w-1/2 p-8 flex items-center justify-center">
      <img
        src="/logistics.png"
        alt="Two people smiling, one handing a box with ClearCycle logo"
        class="object-cover h-full w-full md:w-auto"
      />
    </div>
  </section>
  <footer class="bg-gray-800 text-white text-center py-4">
    <p>&copy; 2025 ClearCycle. All rights reserved.</p>
    <p>Contact us: <a href="mailto:hello@clearcycle.com" class="underline">hello@clearcycle.com</a></p>
  </footer>
</main>

<style>
  html {
    overflow: hidden;
  }
  main {
    overflow-y: hidden;
    scroll-behavior: smooth;
  }
</style>
