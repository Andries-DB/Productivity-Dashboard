<template>
  <div class="space-y-7 w-full">
    <h3 class="text-3xl">Tasks for today</h3>

    <div class="flex flex-col space-y-4">
      <Task 
        v-for="(task, index) in tasks"
        :key="index"
        :task="task"
      />
    </div>
  </div>
</template>

<script setup>
import Task from './Task.vue';

const tasks = [
  {
    name: "Mobile App",
    description: "Prepare Figma File",
    color: "color_1",
    active: true
  },
  {
    name: "Mobile App",
    description: "Research",
    color: "color_3",
    active: false
  },
  {
    name: "UX Wireframes",
    description: "Design UW wireframes",
    color: "color_2",
    active: false
  }
];
</script>