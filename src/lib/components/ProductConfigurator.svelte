<script lang="ts">
  let selectedCategory = 'stem';
</script>

<section class="bg-[#f9f9f7] py-24 px-6">
  <div class="max-w-[1200px] mx-auto text-center">
    <h2 class="text-[40px] font-light text-gray-900 mb-16">
      Every type of learning. <span class="text-gray-400">All in one place.</span>
    </h2>

    <div class="mb-8">
      <h3 class="text-2xl font-normal mb-2">STEM & Robotics</h3>
      <p class="text-gray-500 text-sm">Hands-on science, technology, engineering, and math.</p>
    </div>

    <!-- Event Image -->
    <div class="relative w-full h-[400px] bg-white rounded-xl mb-8 flex items-center justify-center overflow-hidden shadow-sm">
      <div class="absolute inset-0 flex items-center justify-between px-4">
        <button class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center hover:bg-gray-200">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>
        </button>
        <button class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center hover:bg-gray-200">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
        </button>
      </div>
      <img src="/generated/image-children-engaged-in-hands-on-stem-learni-1765523677869-10.webp" class="h-[80%] object-contain" alt="STEM Learning" />
    </div>

    <!-- Category Pills -->
    <div class="flex justify-center gap-4 mb-8 flex-wrap">
      <button class="px-4 py-2 rounded-full bg-primary-100 text-primary-700 border-2 border-primary-500 text-sm font-medium">STEM</button>
      <button class="px-4 py-2 rounded-full bg-gray-100 text-gray-700 text-sm font-medium hover:bg-gray-200">Arts</button>
      <button class="px-4 py-2 rounded-full bg-gray-100 text-gray-700 text-sm font-medium hover:bg-gray-200">Nature</button>
      <button class="px-4 py-2 rounded-full bg-gray-100 text-gray-700 text-sm font-medium hover:bg-gray-200">History</button>
    </div>

    <div class="flex justify-center gap-8 text-sm text-gray-600 mb-4 border-b border-gray-200 pb-4 inline-flex mx-auto w-auto px-12">
      <span>Ages 6-12</span>
      <span>2 hours</span>
      <span>Orlando, FL</span>
    </div>

    <p class="text-xs text-gray-500 mb-8">
      Example event: <span class="font-bold text-gray-900">Amazon Robotics Tour</span><br>
      Most events range from free to $50 per child.
    </p>

    <div class="flex justify-center gap-4">
      <button class="px-6 py-3 bg-gray-100 hover:bg-gray-200 rounded-lg text-sm font-medium transition-colors text-left">
        <span class="block text-[10px] text-gray-500">Explore more</span>
        <span class="text-primary-600">Browse STEM events</span>
      </button>
      <button class="px-6 py-3 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors flex items-center gap-2">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.3-4.3"/></svg>
        Search all events ->
      </button>
    </div>
  </div>
</section>
