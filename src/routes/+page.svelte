<script lang="ts">
  import { onMount } from 'svelte';
  import TopNav from '../components/TopNav.svelte';
  import images from '../lib/json/how-to-request-pickup-images.json';

  let currentIndex = 0;
  let intervalId: any;

  onMount(() => {
    intervalId = setInterval(() => {
      currentIndex = (currentIndex + 1) % images.length;
    }, 3000);
    return () => clearInterval(intervalId);
  });


  function goToPrev() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
  }

  function goToNext() {
    currentIndex = (currentIndex + 1) % images.length;
  }

  function goToSlide(index: number) {
    currentIndex = index;
  }
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

  <section class="min-h-[calc(100vh-4rem)] flex flex-col md:flex-row items-center justify-center bg-gray-100">
    <div style="max-width: 800px; width: 100%; position: relative;">
      <div style="overflow: hidden; width: 100%; height: 400px; position: relative;">
        {#each images as image, i}
          <div
            style="position: absolute; top: 0; left: {i * 100}%; width: 100%; height: 100%; transition: left 0.5s ease-in-out;"
            style:left="{currentIndex === i ? '0' : (i < currentIndex ? '-100%' : '100%')}"
          >
            <img
              src={image.src}
              alt={image.alt}
              style="width: 100%; height: 100%; object-fit: cover; border-radius: 8px;"
            />
            <h3 style="position: absolute; bottom: 20px; left: 20px; color: #FFFFFF; font-size: 1.5rem; font-weight: bold; text-shadow: 1px 1px 2px #000;">
              {image.title}
            </h3>
          </div>
        {/each}
      </div>

      <button
        on:click={goToPrev}
        style="position: absolute; top: 50%; left: 10px; transform: translateY(-50%); background-color: rgba(0, 0, 0, 0.5); color: #FFFFFF; border: none; padding: 10px; border-radius: 50%; cursor: pointer;"
      >
        &lt;
      </button>
      <button
        on:click={goToNext}
        style="position: absolute; top: 50%; right: 10px; transform: translateY(-50%); background-color: rgba(0, 0, 0, 0.5); color: #FFFFFF; border: none; padding: 10px; border-radius: 50%; cursor: pointer;"
      >
        &gt;
      </button>

      <div style="display: flex; justify-content: center; gap: 10px; margin-top: 10px;">
        {#each images as _, i}
          <button
            aria-label="Slide indicator"
            on:click={() => goToSlide(i)}
            style="width: 10px; height: 10px; border-radius: 50%; background-color: {currentIndex === i ? '#109bd4' : '#ccc'}; border: none; cursor: pointer;"
          ></button>
        {/each}
      </div>
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
    overflow-y: auto;
    scroll-behavior: smooth;
  }
</style>
