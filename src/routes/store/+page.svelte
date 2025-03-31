<script>
  import { Button } from 'flowbite-svelte';
  import TopNav from '../../components/TopNav.svelte';
</script>

<TopNav />

<main style="background-color: #E8ECEF;">
  <section style="min-height: calc(100vh - 4rem); padding-top: 0rem;" class="flex flex-col items-center">
    <img
      src="/store-banner.jpg"
      alt="Meeting room with people discussing"
      style="width: 100%; height: 420px; object-fit: cover; margin-bottom: 2rem;"
    />

    <h1 style="color: #4b7163;" class="text-4xl font-bold mb-6">Store</h1>

    <p style="color: #1A2A44;" class="text-lg max-w-2xl text-center">
      Welcome to the ClearCycle Store—where yesterday’s clutter becomes today’s treasure! Dive into a curated stash of pre-loved goods, from quirky furniture to tech gems, all rescued and ready for a new home. Shop smart, save big, and join the cycle of giving stuff a second shot.
    </p>

    <Button style="background-color: #109bd4; margin-top: 2rem;">
      View Store
    </Button>
  </section>
  <footer class="bg-gray-800 text-white text-center py-4">
    <p>&copy; 2025 ClearCycle. All rights reserved.</p>
    <p>Contact us: <a href="mailto:hello@clearcycle.com" class="underline">hello@clearcycle.com</a></p>
  </footer>
</main>
