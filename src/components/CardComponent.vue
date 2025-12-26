<script setup lang="ts">
</script>

<template>
  <div class="bg-white rounded-xl shadow-md border border-gray-200 p-4">
    <!-- Header -->
    <div v-if="$slots.header" class="mb-4">
      <slot name="header" />
    </div>

    <!-- Body -->
    <div class="text-gray-700">
      <slot />
    </div>

    <!-- Footer -->
    <div v-if="$slots.footer" class="mt-4">
      <slot name="footer" />
    </div>
  </div>
</template>


<style scoped>
</style>
