<script>
  import TopNav from '../../components/TopNav.svelte';
</script>

<TopNav />

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
