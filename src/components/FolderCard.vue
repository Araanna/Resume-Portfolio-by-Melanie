<template>
  <div class="relative w-full"> <!-- Container - removed my-[20rem] to fit in grid -->

    <!-- Tab -->
    <div
      class="relative z-10 inline-block rounded-t-3xl border border-purple-300 border-b-0 bg-white px-7 py-1 -mb-[1px]">
      <span class="text-sm font-bold tracking-wide text-purple-500">
        {{ title }}
      </span>
    </div>

    <!-- Right Header Actions Slot -->
    <div class="absolute top-0 right-0 z-10 p-1">
      <slot name="header-actions" />
    </div>

    <!-- Card Body -->
    <div
      class="relative rounded-2xl rounded-tl-none border border-purple-300 bg-white/90 p-8 shadow-xl backdrop-blur-md overflow-hidden">
      <slot />
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
    default: 'Section'
  }
})
</script>
