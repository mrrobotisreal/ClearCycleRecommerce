<script>
  import { Button } from 'flowbite-svelte';
  import TopNav from '../../components/TopNav.svelte';
</script>

<TopNav />

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
