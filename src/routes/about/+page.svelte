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

<main style="background-color: #E8ECEF;">
  <section style="min-height: calc(100vh - 4rem); padding-top: 0rem;" class="flex flex-col items-center">
    <img
      src="/earth-hands.png"
      alt="Earth with grass and dew"
      style="width: 100%; height: 340px; object-fit: cover; margin-bottom: 2rem;"
    />

    <h1 style="color: #1A2A44;" class="text-4xl font-bold mb-6">About ClearCycle</h1>

    <img
      src="/tree-1.png"
      alt="Tree with roots"
      style="width: auto; height: 200px; display: block; margin: 0 auto 2rem auto;"
    />

    <p style="color: #1A2A44;" class="text-lg max-w-2xl text-center">
      At ClearCycle, we’re all about turning your clutter into something meaningful. Founded with a passion for simplifying life, we’ve built a seamless way for you to sell or donate items you no longer need. Our team’s obsessed with logistics—pickup to delivery, we’ve got it dialed—so you can declutter with zero stress. Join us in making letting go a win for you and the planet!
    </p>
  </section>
  <footer class="bg-gray-800 text-white text-center py-4">
    <p>&copy; 2025 ClearCycle. All rights reserved.</p>
    <p>Contact us: <a href="mailto:hello@clearcycle.com" class="underline">hello@clearcycle.com</a></p>
  </footer>
</main>
