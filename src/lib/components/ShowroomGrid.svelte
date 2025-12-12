<script lang="ts">
  import EventCard from "$lib/components/EventCard.svelte";

  const quickBrowseEvents = [
    {
      title: "Marine Biology Beach Exploration",
      image: "/generated/image-diverse-group-of-homeschool-children-col-1765523666086-4.webp",
      date: "Fri, Jan 24",
      time: "9:00 AM - 12:00 PM",
      location: "Clearwater Beach, FL",
      price: "$35",
      category: "Nature",
      ageRange: "7-14"
    },
    {
      title: "Young Entrepreneurs Workshop",
      image: "/generated/image-parent-browsing-on-laptop-with-coffee-re-1765523671935-7.webp",
      date: "Sat, Jan 25",
      time: "1:00 PM - 4:00 PM",
      location: "Orlando, FL",
      price: "$45",
      category: "Business",
      spotsLeft: 2,
      ageRange: "12-17"
    }
  ];
</script>

<section class="bg-[#f9f9f7] pb-24 px-6">
  <div class="max-w-[1400px] mx-auto">
    <div class="mb-12">
      <h2 class="text-3xl font-light text-gray-900 mb-2">Quick browse</h2>
      <p class="text-gray-500">More events happening soon</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-16">
      {#each quickBrowseEvents as event}
        <EventCard {...event} />
      {/each}
    </div>

    <!-- Testimonials -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 border-t border-gray-200 pt-12">
      <div class="col-span-1">
        <h4 class="text-lg text-gray-900">What families are<br>saying about BetterSchool</h4>
      </div>
      
      <div class="col-span-1">
        <p class="text-gray-600 text-sm mb-2">"Finally found amazing local<br>events for our homeschool!"</p>
        <div class="flex text-gray-900 text-xs">★★★★★</div>
      </div>

      <div class="col-span-1">
        <p class="text-gray-600 text-sm mb-2">"BetterSchool makes discovering educational<br>adventures so easy. My kids love it!"</p>
        <div class="flex text-gray-900 text-xs">★★★★★</div>
      </div>
    </div>
  </div>
</section>
