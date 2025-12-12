<script lang="ts">
  import TopBanner from "$lib/components/TopBanner.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import Hero from "$lib/components/Hero.svelte";
  import CategoryNav from "$lib/components/CategoryNav.svelte";
  import Carousel from "$lib/components/Carousel.svelte";
  import ValueProp from "$lib/components/ValueProp.svelte";
  import ShowroomGrid from "$lib/components/ShowroomGrid.svelte";
  import UpcomingEvents from "$lib/components/UpcomingEvents.svelte";
  import LifeWithBackyard from "$lib/components/LifeWithBackyard.svelte";
  import ProductConfigurator from "$lib/components/ProductConfigurator.svelte";
  import PeekInside from "$lib/components/PeekInside.svelte";
  import Steps from "$lib/components/Steps.svelte";
  import Features from "$lib/components/Features.svelte";
  import Illustration from "$lib/components/Illustration.svelte";
  import Sustainability from "$lib/components/Sustainability.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<div class="font-sans antialiased text-gray-900 bg-white">
  <TopBanner />
  <Navbar />
  <main>
    <Hero />
    <CategoryNav />
    <Carousel />
    <ValueProp />
    <ProductConfigurator />
    <UpcomingEvents />
    <ShowroomGrid />
    <Steps />
    <LifeWithBackyard />
    <Features />
    <Illustration />
    <Sustainability />
    <PeekInside />
  </main>
  <Footer />
</div>

