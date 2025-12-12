<script lang="ts">
  import EventCard from "$lib/components/EventCard.svelte";

  const featuredEvents = [
    {
      title: "Amazon Robotics Fulfillment Center Tour",
      image: "/generated/image-children-engaged-in-hands-on-stem-learni-1765523677869-10.webp",
      date: "Sat, Jan 18",
      time: "10:00 AM - 12:00 PM",
      location: "Orlando, FL",
      price: "Free",
      category: "STEM",
      spotsLeft: 3,
      ageRange: "8-14"
    },
    {
      title: "Watercolor Painting Workshop for Kids",
      image: "/generated/image-children-in-an-art-workshop-painting-and-1765523662072-2.webp",
      date: "Sun, Jan 19",
      time: "2:00 PM - 4:00 PM",
      location: "Winter Park, FL",
      price: "$25",
      category: "Arts",
      ageRange: "6-12"
    },
    {
      title: "Natural History Museum Adventure",
      image: "/generated/image-kids-on-an-educational-field-trip-at-a-m-1765523664085-3.webp",
      date: "Tue, Jan 21",
      time: "9:00 AM - 12:00 PM",
      location: "Tampa, FL",
      price: "$15",
      category: "History",
      ageRange: "5-15"
    },
    {
      title: "Hands-On Science Experiments Lab",
      image: "/generated/image-kids-doing-hands-on-science-experiment-o-1765523659862-1.webp",
      date: "Wed, Jan 22",
      time: "3:00 PM - 5:00 PM",
      location: "Orlando, FL",
      price: "$30",
      category: "STEM",
      spotsLeft: 2,
      ageRange: "7-13"
    }
  ];
</script>

<section class="bg-white py-16 px-6">
  <div class="max-w-[1400px] mx-auto">
    <div class="flex items-center justify-between mb-8">
      <div>
        <h2 class="text-3xl font-light text-gray-900 mb-2">Featured events this week</h2>
        <p class="text-gray-500">Popular educational experiences near you</p>
      </div>
      <button class="px-6 py-3 border-2 border-gray-200 hover:border-gray-300 rounded-lg text-sm font-medium transition-colors">
        View all events →
      </button>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
      {#each featuredEvents as event}
        <EventCard {...event} />
      {/each}
    </div>
  </div>
</section>
