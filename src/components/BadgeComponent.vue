<script setup lang="ts">
defineProps<{
  msg: string,
  additional_class: string
}>()
</script>

<template>
    <div class="badge flex justify-end items-center round rounded-lg p-1" :class="additional_class">
        <span>&#9679; &nbsp;</span>
        <span>{{msg}}</span>
    </div>
</template>


<style scoped>
  .badge span {
    font-size: 8px; 
    font-weight: bold;
    text-transform: uppercase;
  }
  .active {
    background-color: #d0fadf;
    color: #0dc058;
  }
</style>
