<script lang="ts">
  import { page } from '$app/stores';
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Skeleton } from 'flowbite-svelte';
  $: activeUrl = $page.url.pathname;

  let hoverStates: { [key: string]: boolean } = {
    '/': false,
    '/about': false,
    '/partners': false,
    '/careers': false,
    '/store': false
  };

  function getLinkStyle(href: string): string {
    const isActive: boolean = activeUrl === href;
    const isHovered: boolean = hoverStates[href as keyof typeof hoverStates];
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
