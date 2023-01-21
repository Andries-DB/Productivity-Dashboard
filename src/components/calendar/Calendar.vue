<template>
  <div class="space-yy-5">
    <div class="flex justify-between items-center">
      <h3 class="text-xl font-bold">Calendar</h3>
      <button class="relative p-2 bg-white rounded-xl"> 
        <mdicon name="bell"/>
        <span class="absolute bg-red-400 top-2 right-2 h-2 w-2 rounded-full"></span>
      </button>
    </div>

    <div class="space-y-7">

      <div v-for="i in 3" :key="i">
        <div class="flex justify-between">
          <h5 class="font-bol text-gray-600">January 23, 2023</h5>
          <mdicon name="dots-vertical" />
        </div>

        <div 
          v-for="j in 4" 
          :key="j"
          class="flex justify-between items-center gap-4 ">
          <p class="w-24 text-xl">10h</p>
          <div class="w-1 rounded-xl h-10" :class="`bg-color_${(i+j) % 3 + 1}`" />

          <div class="flex-1">
            <p class="font-bold text-gray-800 text-xl">Design</p>
            <p class="text-gray-500">Facebook Brand</p>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>