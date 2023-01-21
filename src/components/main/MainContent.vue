<script setup>
  import HelloBar from './HelloBar.vue';
</script>

<template>
<div class="flex flex-col gap-10 p-7">
  <div>
    <HelloBar />
  </div>

  <div class="bg-debug">Current Projects</div>
  <div class="grid grid-cols-12 grid-rows-2 gap-10 h-full">
    <div class="row-span-2 col-span-12 md:col-span-6 bg-debug">TasksforToday</div>
    <div class="row-span-1 col-span-12 md:col-span-6 bg-debug">Statistics</div>
    <div class="row-span-1 col-span-12 md:col-span-6 bg-debug">Pro Plan</div>
  </div>
</div>
</template>