<script setup>
defineProps({
  'index' : Number,
})
</script>
<template>
  <div class="flex flex-col pt-24 content-center place-items-center align-middle items-center w-12/12">
    <div class="w-12/12 lg:w-6-12 relative focus-within:ring-2 focus-within:ring-indigo-500">
      <h3 class="text-sm font-semibold text-gray-800">
        <div class="hover:underline focus:outline-none">
          <!-- Extend touch target to entire panel -->
          <span class="absolute inset-0" aria-hidden="true"></span>
          <slot name="heading"></slot>
        </div>
      </h3>
      <p class="mt-1 text-sm text-gray-600 line-clamp-2"><slot></slot></p>
    </div>
  </div>
</template>

<style scoped>
</style>
