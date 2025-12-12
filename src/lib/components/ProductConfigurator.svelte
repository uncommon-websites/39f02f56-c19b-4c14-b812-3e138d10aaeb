<script lang="ts">
  import EventCard from "$lib/components/EventCard.svelte";

  const categories = [
    { id: 'stem', name: 'STEM & Robotics', desc: 'Hands-on science, technology, engineering, and math' },
    { id: 'arts', name: 'Arts & Crafts', desc: 'Creative workshops and artistic expression' },
    { id: 'nature', name: 'Nature & Outdoors', desc: 'Explore the natural world together' },
    { id: 'history', name: 'History & Culture', desc: 'Discover our past through immersive experiences' }
  ];

  const eventsByCategory = {
    stem: [
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
        title: "Hands-On Science Experiments Lab",
        image: "/generated/image-kids-doing-hands-on-science-experiment-o-1765523659862-1.webp",
        date: "Wed, Jan 22",
        time: "3:00 PM - 5:00 PM",
        location: "Orlando, FL",
        price: "$30",
        category: "STEM",
        ageRange: "7-13"
      },
      {
        title: "Coding for Kids: Build Your First Game",
        image: "/generated/image-children-engaged-in-hands-on-stem-learni-1765523677869-10.webp",
        date: "Thu, Jan 23",
        time: "4:00 PM - 6:00 PM",
        location: "Tampa, FL",
        price: "$35",
        category: "STEM",
        ageRange: "9-15"
      }
    ],
    arts: [
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
        title: "Clay Sculpture & Pottery Making",
        image: "/generated/image-children-in-an-art-workshop-painting-and-1765523662072-2.webp",
        date: "Sat, Jan 25",
        time: "10:00 AM - 1:00 PM",
        location: "Orlando, FL",
        price: "$40",
        category: "Arts",
        spotsLeft: 4,
        ageRange: "8-14"
      }
    ],
    nature: [
      {
        title: "Wildlife Sanctuary Nature Walk",
        image: "/generated/image-diverse-group-of-homeschool-children-col-1765523666086-4.webp",
        date: "Sat, Jan 18",
        time: "8:00 AM - 11:00 AM",
        location: "Kissimmee, FL",
        price: "$20",
        category: "Nature",
        ageRange: "5-12"
      }
    ],
    history: [
      {
        title: "Natural History Museum Adventure",
        image: "/generated/image-kids-on-an-educational-field-trip-at-a-m-1765523664085-3.webp",
        date: "Tue, Jan 21",
        time: "9:00 AM - 12:00 PM",
        location: "Tampa, FL",
        price: "$15",
        category: "History",
        ageRange: "5-15"
      }
    ]
  };

  let selectedCategory = $state('stem');
  let currentEvents = $derived(eventsByCategory[selectedCategory as keyof typeof eventsByCategory]);
  let currentCategoryInfo = $derived(categories.find(c => c.id === selectedCategory));
</script>

<section class="bg-[#f9f9f7] py-24 px-6">
  <div class="max-w-[1400px] mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-[40px] font-light text-gray-900 mb-4">
        Browse events by category
      </h2>
      <p class="text-gray-500 text-lg">Every type of learning experience in one place</p>
    </div>

    <!-- Category Pills -->
    <div class="flex justify-center gap-4 mb-12 flex-wrap">
      {#each categories as category}
        <button 
          class={[
            'px-6 py-3 rounded-full text-sm font-medium transition-all',
            selectedCategory === category.id
              ? 'bg-primary-600 text-white'
              : 'bg-white border-2 border-gray-200 text-gray-700 hover:border-gray-300'
          ]}
          onclick={() => selectedCategory = category.id}
        >
          {category.name}
        </button>
      {/each}
    </div>

    {#if currentCategoryInfo}
      <div class="text-center mb-8">
        <h3 class="text-2xl font-normal mb-2">{currentCategoryInfo.name}</h3>
        <p class="text-gray-500 text-sm">{currentCategoryInfo.desc}</p>
      </div>
    {/if}

    <!-- Events Grid -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
      {#each currentEvents as event}
        <EventCard {...event} />
      {/each}
    </div>

    <div class="text-center">
      <button class="px-8 py-4 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors inline-flex items-center gap-2">
        View all {currentCategoryInfo?.name.toLowerCase()} events
        <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m9 18 6-6-6-6"/></svg>
      </button>
    </div>
  </div>
</section>
