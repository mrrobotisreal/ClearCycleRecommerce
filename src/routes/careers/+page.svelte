<script>
  import { page } from '$app/stores';
  import { Button, Navbar, NavBrand, NavLi, NavUl, NavHamburger, Skeleton } from 'flowbite-svelte';
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
      src="/careers-banner.jpg"
      alt="Meeting room with people discussing"
      style="width: 100%; height: 420px; object-fit: cover; margin-bottom: 2rem;"
    />

    <h1 style="color: #4b7163;" class="text-4xl font-bold mb-6">ClearCycle Careers</h1>

    <p style="color: #1A2A44;" class="text-lg max-w-2xl text-center">
      Ready to make a dent in the clutter universe? At ClearCycle, you’ll join a crew obsessed with turning chaos into opportunity—think fast-paced logistics, big-impact sustainability, and a vibe that’s all about teamwork and innovation. We’re not just moving stuff; we’re reshaping how people let go, and you’ll be at the heart of it with a team that’s got your back and a mission that matters.
    </p>

    <Button style="background-color: #109bd4; margin-top: 2rem;">
      Join The Team
    </Button>
  </section>
  <footer class="bg-gray-800 text-white text-center py-4">
    <p>&copy; 2025 ClearCycle. All rights reserved.</p>
    <p>Contact us: <a href="mailto:hello@clearcycle.com" class="underline">hello@clearcycle.com</a></p>
  </footer>
</main>
