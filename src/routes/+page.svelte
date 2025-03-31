<script lang="ts">
  import TopNav from '../components/TopNav.svelte';
</script>

<TopNav />

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
