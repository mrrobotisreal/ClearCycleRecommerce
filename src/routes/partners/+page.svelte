<script>
  import { Card } from 'flowbite-svelte';
  import TopNav from '../../components/TopNav.svelte';
</script>

<TopNav />

<main style="background-color: #E8ECEF;">
  <section style="min-height: calc(100vh - 4rem); padding-top: 0rem; background-color: #FFFFFF;" class="flex flex-col items-center">
    <div style="position: relative; width: 100%; height: 400px; margin-bottom: 2rem;">
      <img
        src="/Shaking-hands-networking.png"
        alt="Earth with grass and dew"
        style="width: 100%; height: 400px; object-fit: cover;"
      />
      <a
        href="/become-partner"
        style="position: absolute; bottom: 30px; left: 80px; background-color: #109bd4; color: #FFFFFF; padding: 12px 24px; border-radius: 8px; font-weight: bold; text-decoration: none;"
      >
        Become A Partner
      </a>
    </div>

    <h1 style="color: #1A2A44;" class="text-4xl font-bold mb-6">Simplified. Verified. Satisfied.</h1>

    <p style="color: #1A2A44;" class="text-lg max-w-2xl text-center">
      ClearCycle rolls with the big names you know and trust—think top-tier logistics, retail giants, and eco-champions—all vetted so you don’t have to sweat it. Our partner network is a fortress of reliability, streamlining your declutter game while connecting you to companies that get it done right. Trust us, because they do.
    </p>
  </section>
  <section style="min-height: calc(100vh - 4rem); padding-top: 2rem; background-color: #E8ECEF; width: 100%;" class="flex flex-col items-center">
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2rem; max-width: 1200px; margin: 0 auto;">
      <Card img="/commercial-real-estate.webp" style="width: 360px; height: 540px; position: relative;">
        <h5 style="position: absolute; top: 10px; color: #ffffff; font-size: 1.5rem; font-weight: bold; text-shadow: 1px 1px 2px #000000;">
          Commercial Real Estate
        </h5>
        <p style="color: #1A2A44; margin-top: 1rem; margin-bottom: 1rem; font-weight: bold;">
          Need to clear a space? We’ll swoop in, snag the unwanted furniture, and banish clutter faster than you can say “open house.”
        </p>
        <ul style="color: #1A2A44; list-style-type: disc; padding-left: 1.5rem;">
          <li>We cut the junk, making staging a breeze.</li>
          <li>No pickup fee—we clear it for free.</li>
        </ul>
      </Card>
      <Card img="/junk-hauler.jpg" style="width: 360px; height: 540px; position: relative;">
        <h5 style="position: absolute; top: 10px; color: #ffffff; font-size: 1.5rem; font-weight: bold; text-shadow: 1px 1px 2px #000000;">
          Junk Hauler
        </h5>
        <p style="color: #1A2A44; margin-top: 1rem; margin-bottom: 1rem; font-weight: bold;">
          Got a haul too big to handle? We’ll take it off your truck and turn your load into someone else’s treasure.
        </p>
        <ul style="color: #1A2A44; list-style-type: disc; padding-left: 1.5rem;">
          <li>We lighten your load with zero hassle.</li>
          <li>Free pickups—keep your profits, ditch the junk.</li>
        </ul>
      </Card>
      <Card img="/furniture-store.jpg" style="width: 360px; height: 540px; position: relative;">
        <h5 style="position: absolute; top: 10px; color: #ffffff; font-size: 1.5rem; font-weight: bold; text-shadow: 1px 1px 2px #000000;">
          Furniture Store
        </h5>
        <p style="color: #1A2A44; margin-top: 1rem; margin-bottom: 1rem; font-weight: bold;">
          Old stock piling up? We’ll clear out yesterday’s chairs so you can showcase today’s style without the clutter.
        </p>
        <ul style="color: #1A2A44; list-style-type: disc; padding-left: 1.5rem;">
          <li>We streamline inventory turnover.</li>
          <li>No cost pickup—more space, no expense.</li>
        </ul>
      </Card>
    </div>

    <h2 style="color: #4b7163; margin-top: 2rem;" class="text-4xl font-bold mb-6 mt-12">Our Trusted Partners</h2>

    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2rem; width: 100%; margin-top: 1rem;">
      <img
        src="/DTG_350.webp"
        alt="DTG"
        style="width: 180px; height: auto; margin: 10px; object-fit: cover;"
      />
      <img
        src="/offeruplogo-1.webp"
        alt="OfferUp"
        style="width: 240px; height: auto; margin: 10px; object-fit: cover;"
      />
      <img
        src="/1-800-GOT-JUNK_large.webp"
        alt="1-800-GOT-JUNK"
        style="width: 380px; height: auto; margin: 10px; object-fit: cover;"
      />
    </div>
  </section>
  <footer class="bg-gray-800 text-white text-center py-4">
    <p>&copy; 2025 ClearCycle. All rights reserved.</p>
    <p>Contact us: <a href="mailto:hello@clearcycle.com" class="underline">hello@clearcycle.com</a></p>
  </footer>
</main>
