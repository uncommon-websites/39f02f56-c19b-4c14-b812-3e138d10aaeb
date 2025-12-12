<script lang="ts">
</script>

<section class="bg-white pt-16 pb-0">
  <div class="max-w-[1400px] mx-auto px-6 mb-8">
    <div class="text-center mb-8">
      <h1 class="text-[72px] leading-none font-light tracking-tight mb-4">
        Discover local<br>
        <span class="text-primary-600">educational events</span>
      </h1>
      <p class="text-gray-600 text-xl font-light mb-8">
        Browse thousands of vetted learning experiences for your family
      </p>

      <!-- Search Bar -->
      <div class="max-w-[900px] mx-auto bg-white border-2 border-gray-200 rounded-xl p-3 flex flex-col md:flex-row gap-3">
        <div class="flex-1 flex items-center gap-3 px-4 py-2 border-r border-gray-200">
          <svg class="w-5 h-5 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.3-4.3"/></svg>
          <input 
            type="text" 
            placeholder="Search events, activities, or topics..." 
            class="w-full outline-none text-gray-900 placeholder-gray-400"
          />
        </div>
        <div class="flex-1 flex items-center gap-3 px-4 py-2 border-r border-gray-200">
          <svg class="w-5 h-5 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
          <input 
            type="text" 
            placeholder="Orlando, FL" 
            class="w-full outline-none text-gray-900 placeholder-gray-400"
          />
        </div>
        <div class="flex items-center gap-3 px-4 py-2">
          <svg class="w-5 h-5 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="4" width="18" height="18" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/></svg>
          <select class="outline-none text-gray-900 bg-transparent">
            <option>Any date</option>
            <option>This week</option>
            <option>This month</option>
          </select>
        </div>
        <button class="px-8 py-3 bg-primary-600 hover:bg-primary-700 text-white rounded-lg font-medium transition-colors">
          Search
        </button>
      </div>

      <!-- Quick Stats -->
      <div class="flex justify-center gap-8 mt-6 text-sm text-gray-500">
        <span><strong class="text-gray-900">1,200+</strong> events</span>
        <span><strong class="text-gray-900">10,000+</strong> families</span>
        <span><strong class="text-gray-900">500+</strong> organizers</span>
      </div>
    </div>
  </div>

  <!-- Hero Image -->
  <div class="w-full h-[500px] bg-gray-200 overflow-hidden relative">
    <img 
      src="/generated/image-children-and-parents-at-an-educational-r-1765523657715-0.webp" 
      alt="Children and parents at educational event" 
      class="w-full h-full object-cover"
    />
    <div class="absolute inset-0 bg-gradient-to-t from-black/40 to-transparent"></div>
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 text-center">
      <p class="text-white text-lg font-light">Trusted by homeschool and traditional families across Florida</p>
    </div>
  </div>
</section>
