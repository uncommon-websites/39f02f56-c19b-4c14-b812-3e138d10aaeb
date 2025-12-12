<script lang="ts">
  type Props = {
    title: string;
    image: string;
    date: string;
    time: string;
    location: string;
    price: string;
    category: string;
    spotsLeft?: number;
    ageRange?: string;
  };

  let { 
    title, 
    image, 
    date, 
    time, 
    location, 
    price, 
    category,
    spotsLeft,
    ageRange
  }: Props = $props();
</script>

<div class="bg-white rounded-xl overflow-hidden border border-gray-200 hover:border-primary-300 transition-all duration-300 group cursor-pointer">
  <!-- Event Image -->
  <div class="relative h-48 overflow-hidden bg-gray-100">
    <img 
      src={image} 
      alt={title} 
      class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
    />
    <div class="absolute top-3 left-3 bg-white px-3 py-1 rounded-full text-xs font-medium text-gray-900">
      {category}
    </div>
    {#if spotsLeft && spotsLeft < 5}
      <div class="absolute top-3 right-3 bg-primary-600 text-white px-3 py-1 rounded-full text-xs font-medium">
        {spotsLeft} spots left
      </div>
    {/if}
  </div>

  <!-- Event Details -->
  <div class="p-5">
    <h3 class="text-lg font-medium text-gray-900 mb-3 line-clamp-2 group-hover:text-primary-600 transition-colors">
      {title}
    </h3>

    <div class="space-y-2 mb-4">
      <div class="flex items-center gap-2 text-sm text-gray-600">
        <svg class="w-4 h-4 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="4" width="18" height="18" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/></svg>
        <span>{date}</span>
      </div>
      <div class="flex items-center gap-2 text-sm text-gray-600">
        <svg class="w-4 h-4 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
        <span>{time}</span>
      </div>
      <div class="flex items-center gap-2 text-sm text-gray-600">
        <svg class="w-4 h-4 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
        <span class="line-clamp-1">{location}</span>
      </div>
      {#if ageRange}
        <div class="flex items-center gap-2 text-sm text-gray-600">
          <svg class="w-4 h-4 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75"/></svg>
          <span>Ages {ageRange}</span>
        </div>
      {/if}
    </div>

    <div class="flex items-center justify-between pt-4 border-t border-gray-100">
      <div>
        <div class="text-xs text-gray-500 mb-1">From</div>
        <div class="text-xl font-medium text-gray-900">{price}</div>
      </div>
      <button class="px-5 py-2 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors">
        Book now
      </button>
    </div>
  </div>
</div>
