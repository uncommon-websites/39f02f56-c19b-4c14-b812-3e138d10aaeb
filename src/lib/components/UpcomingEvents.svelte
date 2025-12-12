<script lang="ts">
  import EventCard from "$lib/components/EventCard.svelte";

  const upcomingEvents = [
    {
      title: "Astronomy Night: Stargazing & Telescopes",
      image: "/generated/image-diverse-group-of-homeschool-children-col-1765523666086-4.webp",
      date: "Fri, Jan 31",
      time: "7:00 PM - 9:00 PM",
      location: "Orlando, FL",
      price: "$20",
      category: "Science",
      ageRange: "8-16"
    },
    {
      title: "Shakespeare for Kids: Acting Workshop",
      image: "/generated/image-children-in-an-art-workshop-painting-and-1765523662072-2.webp",
      date: "Sat, Feb 1",
      time: "10:00 AM - 1:00 PM",
      location: "Winter Park, FL",
      price: "$40",
      category: "Arts",
      spotsLeft: 3,
      ageRange: "9-14"
    },
    {
      title: "Robotics Competition Prep Workshop",
      image: "/generated/image-children-engaged-in-hands-on-stem-learni-1765523677869-10.webp",
      date: "Sun, Feb 2",
      time: "2:00 PM - 5:00 PM",
      location: "Tampa, FL",
      price: "$50",
      category: "STEM",
      ageRange: "10-16"
    },
    {
      title: "Farm-to-Table Cooking Class",
      image: "/generated/image-kids-doing-hands-on-science-experiment-o-1765523659862-1.webp",
      date: "Mon, Feb 3",
      time: "3:00 PM - 5:30 PM",
      location: "Orlando, FL",
      price: "$35",
      category: "Life Skills",
      ageRange: "7-13"
    },
    {
      title: "Historical Reenactment: Colonial America",
      image: "/generated/image-kids-on-an-educational-field-trip-at-a-m-1765523664085-3.webp",
      date: "Tue, Feb 4",
      time: "10:00 AM - 2:00 PM",
      location: "St. Augustine, FL",
      price: "$30",
      category: "History",
      spotsLeft: 4,
      ageRange: "8-14"
    }
  ];
</script>

<section class="bg-white py-24 px-6">
  <div class="max-w-[1400px] mx-auto">
    <div class="flex items-center justify-between mb-8">
      <div>
        <h2 class="text-3xl font-light text-gray-900 mb-2">Upcoming events</h2>
        <p class="text-gray-500">Don't miss these popular experiences</p>
      </div>
      <div class="flex gap-2">
        <button class="w-10 h-10 rounded-full border-2 border-gray-200 hover:border-gray-300 flex items-center justify-center transition-colors">
          <svg class="w-5 h-5 text-gray-600" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m15 18-6-6 6-6"/></svg>
        </button>
        <button class="w-10 h-10 rounded-full border-2 border-gray-200 hover:border-gray-300 flex items-center justify-center transition-colors">
          <svg class="w-5 h-5 text-gray-600" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m9 18 6-6-6-6"/></svg>
        </button>
      </div>
    </div>

    <div class="flex gap-6 overflow-x-auto pb-4 snap-x scrollbar-hide">
      {#each upcomingEvents as event}
        <div class="min-w-[320px] snap-center">
          <EventCard {...event} />
        </div>
      {/each}
    </div>

    <div class="text-center mt-8">
      <button class="px-8 py-4 border-2 border-gray-200 hover:border-gray-300 rounded-lg text-sm font-medium transition-colors">
        View full calendar →
      </button>
    </div>
  </div>
</section>

<style>
  .scrollbar-hide::-webkit-scrollbar {
    display: none;
  }
  .scrollbar-hide {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
</style>
