<script lang="ts">
  const categories = [
    { name: "STEM", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M10 2v7.527a2 2 0 0 1-.211.896L4.72 20.55a1 1 0 0 0 .9 1.45h12.76a1 1 0 0 0 .9-1.45l-5.069-10.127A2 2 0 0 1 14 9.527V2"/><path d="M8.5 2h7"/><path d="M7 16h10"/></svg>', count: 234 },
    { name: "Arts", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="13.5" cy="6.5" r=".5"/><circle cx="17.5" cy="10.5" r=".5"/><circle cx="8.5" cy="7.5" r=".5"/><circle cx="6.5" cy="12.5" r=".5"/><path d="M12 2C6.5 2 2 6.5 2 12s4.5 10 10 10c.926 0 1.648-.746 1.648-1.688 0-.437-.18-.835-.437-1.125-.29-.289-.438-.652-.438-1.125a1.64 1.64 0 0 1 1.668-1.668h1.996c3.051 0 5.555-2.503 5.555-5.554C21.965 6.012 17.461 2 12 2z"/></svg>', count: 156 },
    { name: "Nature", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 13v8M17 8c0-2.76-2.46-5-5.5-5S6 5.24 6 8h11Z"/><path d="M12 8c0-2.76-2.46-5-5.5-5S1 5.24 1 8h11Z"/><path d="M12 8c0-2.76 2.48-5 5.5-5s5.5 2.24 5.5 5h-11Z"/></svg>', count: 98 },
    { name: "History", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M6 22V4a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v18Z"/><path d="M6 12H4a2 2 0 0 0-2 2v6a2 2 0 0 0 2 2h2"/><path d="M18 9h2a2 2 0 0 1 2 2v9a2 2 0 0 1-2 2h-2"/><path d="M10 6h4"/><path d="M10 10h4"/><path d="M10 14h4"/><path d="M10 18h4"/></svg>', count: 87 },
    { name: "Music", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 18V5l12-2v13"/><circle cx="6" cy="18" r="3"/><circle cx="18" cy="16" r="3"/></svg>', count: 123 },
    { name: "Sports", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m6.5 6.5 11 11"/><path d="m21 21-1-1"/><path d="m3 3 1 1"/><path d="m18 22 4-4"/><path d="m2 6 4-4"/><path d="m3 10 7-7"/><path d="m14 21 7-7"/></svg>', count: 145 },
    { name: "Reading", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"/><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"/></svg>', count: 76 },
    { name: "All Events", svg: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"/><path d="M5 3v4"/><path d="M19 17v4"/><path d="M3 5h4"/><path d="M17 19h4"/></svg>', count: 1200 }
  ];

  let selectedCategory = $state("All Events");
</script>

<section class="bg-white border-b border-gray-200 py-6 px-6">
  <div class="max-w-[1400px] mx-auto">
    <div class="flex items-center justify-between mb-4">
      <h3 class="text-sm font-medium text-gray-900">Browse by category</h3>
      <button class="text-xs text-primary-600 hover:text-primary-700">View all categories →</button>
    </div>
    
    <div class="flex gap-3 overflow-x-auto pb-2 scrollbar-hide">
      {#each categories as category}
        <button 
          class={[
            'flex flex-col items-center gap-2 px-6 py-4 rounded-xl border-2 transition-all min-w-[120px]',
            selectedCategory === category.name 
              ? 'bg-primary-50 border-primary-500 text-primary-700' 
              : 'bg-white border-gray-200 text-gray-700 hover:border-gray-300'
          ]}
          onclick={() => selectedCategory = category.name}
        >
          {@html category.svg.replace('<svg', '<svg class="w-6 h-6"')}
          <div class="text-center">
            <div class="text-sm font-medium">{category.name}</div>
            <div class="text-xs text-gray-500">{category.count}</div>
          </div>
        </button>
      {/each}
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
