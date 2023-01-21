<script setup>
  import NavBarMenu from './NavBarMenu.vue';
  import {ref} from 'vue';

  const MOBILE_BREAKPOINT = 1024; //tailwind lg
  const width = ref(document.body.offsetWidth);
  const menuIsActive = ref(width.value > MOBILE_BREAKPOINT);

  const toggleMenu = () => {
    menuIsActive.value = !menuIsActive.value;
  }

  window.addEventListener('resize', () => {
    width.value = document.body.offsetWidth;
    menuIsActive.value = width.value > MOBILE_BREAKPOINT;
  });
</script>

<template>
  <div class="lg:space-y-10 lg:block relative grid grid-cols-12 border-r-2 h-full">
    <div class="col-span-9 flex justify-center items-center gap-4">
      <div class="bg-gradient-to-tl from-color_3 to-pink-500 rounded-xl p-2 text-white">
        <mdicon name="checkbox-marked-circle-plus-outline" class="text-current"/>
      </div>
      <strong>Producteevy</strong>
    </div>

    <div class="lg:hidden block col-span-3 flex justify-end items-center p-2">
      <button class="bg-stone-300 rounded-lg p-2" @click="toggleMenu">
        <mdicon name="menu" />
      </button>
    </div>

    <div class="col-span-12 hidden lg:block pt-5">
      <div class="relative w-full h-24 flex flex-col items-center gap-4">
        <img src="../../assets/Sara.jpg" alt="Sara" class="w-24 h-24 rounded-full">
        <p class="absolute bg-white -bottom-2 px-2 py-1 text-xs text-orange-500 flex items-center gap-1 rounded-full">
          <mdicon name="clock" width="20px"/>
          <span class="font-bold">10h</span>
        </p>
      </div>

      <div class="text-center">
        <h1 class="font-bold text-black">Sara Connor</h1>
        <a href="#" class="text-gray-500 ">sara.connor@gmail.com</a>
      </div>
    </div>
    <div class="col-span-12 p-10 mb-20" v-if="menuIsActive">
      <NavBarMenu />
    </div>

    <div class="hidden lg:block absolute bottom-0 left-0 p-2">
      <img src="../../assets/navbar.svg" alt="Logo">
    </div>
  </div>
</template>
