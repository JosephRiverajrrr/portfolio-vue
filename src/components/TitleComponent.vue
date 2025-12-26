<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<template> 
 <div class="flex gap-1">
    <span class="text-md font-semibold text-gray-500">&#9679; </span>
    <p class="text-md font-semibold text-gray-700">{{title}}</p>
  </div>
</template>


<style scoped> 
</style>
