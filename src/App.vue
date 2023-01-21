<script setup>
import Navbar from './components/navigation/NavBar.vue'
import MainContent from './components/main/MainContent.vue'
import Calendar from './components/calendar/Calendar.vue'
</script>

<template>
  <div class="grid grid-cols-12 gap-2 h-screen overflow-hidden">
    <div class="col-span-12 lg:col-span-9 bg-stone-50 rounded-r-[37px] flex gap-2 md:divide-x-2 flex-col lg:flex-row">
      <div class="lg:w-[250px] w-full lg:h-full overflow-hidden">
        <Navbar />
      </div>
      <div class="flex-1 overflow-hidden">
        <MainContent />
      </div>
    </div>
    <div class="col-span-3 hidden">
      <div class="">
        <Calendar />
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>