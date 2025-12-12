<script lang="ts">
  const steps = [
    {
      num: "01",
      title: "Discover",
      desc: "Browse vetted educational events in your area. Filter by age, interest, and location.",
      img: "/generated/image-parent-browsing-on-laptop-with-coffee-re-1765523671935-7.webp"
    },
    {
      num: "02",
      title: "Book",
      desc: "Reserve your spot with just a few clicks. Get instant confirmation and event details.",
      img: "/generated/image-kids-on-an-educational-field-trip-at-a-m-1765523664085-3.webp"
    },
    {
      num: "03",
      title: "Attend",
      desc: "Show up and enjoy hands-on learning experiences with your family and community.",
      img: "/generated/image-family-arriving-at-an-educational-event--1765523673871-8.webp"
    },
    {
      num: "04",
      title: "Connect",
      desc: "Build friendships, share experiences, and discover new learning adventures together.",
      img: "/generated/image-diverse-group-of-homeschool-children-col-1765523666086-4.webp"
    }
  ];
</script>

<section class="bg-white py-24 px-6">
  <div class="max-w-[1200px] mx-auto">
    <h2 class="text-[40px] leading-tight font-light text-gray-900 mb-16 max-w-[600px]">
      Finding educational events is as easy as booking a ticket.
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
      {#each steps as step}
        <div class="flex flex-col">
          <div class="bg-black text-white text-xs font-bold w-8 h-8 flex items-center justify-center rounded mb-6">
            {step.num}
          </div>
          <h3 class="text-xl font-normal mb-2">{step.title}</h3>
          <p class="text-gray-500 text-sm leading-relaxed mb-6 min-h-[80px]">{step.desc}</p>
          <div class="rounded-xl overflow-hidden h-[200px] bg-gray-100">
            <img src={step.img} alt={step.title} class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-500" />
          </div>
        </div>
      {/each}
    </div>

    <div class="bg-[#f9f9f7] rounded-2xl p-12 flex flex-col md:flex-row items-center justify-between gap-8">
      <div>
        <h3 class="text-2xl font-light mb-2">Want to create events?</h3>
        <p class="text-gray-500 text-sm">Learn how to become an event organizer and share your passion.</p>
      </div>
      <div class="flex gap-4">
        <button class="px-6 py-3 bg-white border border-gray-200 hover:bg-gray-50 rounded-lg text-sm font-medium transition-colors">
          Organizer guide
        </button>
        <button class="px-6 py-3 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors flex items-center gap-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><line x1="19" x2="19" y1="8" y2="14"/><line x1="22" x2="16" y1="11" y2="11"/></svg>
          Become an organizer
        </button>
      </div>
    </div>
  </div>
</section>
