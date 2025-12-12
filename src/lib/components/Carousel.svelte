<script lang="ts">
  const images = [
    {
      src: "/generated/image-kids-doing-hands-on-science-experiment-o-1765523659862-1.webp",
      title: "Science & Nature",
      desc: "Hands-on experiments"
    },
    {
      src: "/generated/image-children-in-an-art-workshop-painting-and-1765523662072-2.webp",
      title: "Arts & Crafts",
      desc: "Creative workshops"
    },
    {
      src: "/generated/image-kids-on-an-educational-field-trip-at-a-m-1765523664085-3.webp",
      title: "Museum Tours",
      desc: "Cultural experiences"
    }
  ];
</script>

<section class="bg-white pb-24 overflow-hidden">
  <div class="flex gap-4 overflow-x-auto px-6 pb-8 snap-x">
    {#each images as img}
      <div class="min-w-[80vw] md:min-w-[60vw] lg:min-w-[45vw] h-[400px] snap-center first:pl-0">
        <img src={img.src} alt={img.title} class="w-full h-full object-cover rounded-lg" />
      </div>
    {/each}
  </div>
  
  <div class="text-center mt-4">
    <p class="text-gray-500 text-sm mb-4">Explore diverse educational experiences <span class="text-gray-400">in your area</span></p>
    <div class="flex justify-center gap-2">
      <div class="w-1.5 h-1.5 rounded-full bg-gray-800"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
      <div class="w-1.5 h-1.5 rounded-full bg-gray-300"></div>
    </div>
  </div>
</section>
