<script setup>
import { ref } from 'vue';

// 用於追蹤目前開啟的是哪個下拉選單
const openMenuKey = ref(null);

// 切換下拉選單狀態的函式
const toggleMenu = (key) => {
  // 如果再次點擊已經開啟的選單，就將其關閉
  if (openMenuKey.value === key) {
    openMenuKey.value = null;
  } else {
    // 否則，開啟新的選單
    openMenuKey.value = key;
  }
};
</script>

<template>
  <header class="bg-gray-100 w-md font-sans">

    <div class="container mx-auto flex items-center justify-between py-3 px-4 sm:px-6">
      <div class="flex items-center space-x-4">
        <img src="/images/hospital.png" alt="醫院 Logo" class="h-20 w-auto" />
        <span class="text-lg font-bold p-5 text-gray-800 hidden md:block">
          臺中市立老人復健綜合醫院
        </span>
      </div>

      <div class="flex items-center space-x-4">
        <div class="relative hidden sm:block">
          <input
              type="text"
              placeholder="全站搜尋"
              class="w-48 rounded-full border border-gray-300 bg-gray-100 py-1.5 pl-4 pr-10 text-sm focus:outline-none focus:ring-2 focus:ring-teal-500"
          />
          <div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
            <svg class="w-5 h-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M10,18c1.846,0,3.543-0.635,4.897-1.688l4.396,4.396l1.414-1.414l-4.396-4.396C17.365,13.543,18,11.846,18,10 c0-4.411-3.589-8-8-8s-8,3.589-8,8S5.589,18,10,18z M10,4c3.309,0,6,2.691,6,6s-2.691,6-6,6s-6-2.691-6-6S6.691,4,10,4z"></path></svg>
          </div>
        </div>
      </div>
    </div>

    <nav class="bg-teal-600 text-white">
      <div class="container mx-auto">
        <ul class="flex w-full">

          <li class="relative flex-1 text-center">
            <button @click="toggleMenu('about')" class="w-full flex justify-center items-center py-4 px-3 hover:bg-teal-700 transition-colors duration-200">
              <span>醫院介紹</span>
              <svg class="w-4 h-4 ml-1.5 transition-transform duration-300" :class="{ 'rotate-180': openMenuKey === 'about' }" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </button>
            <ul v-if="openMenuKey === 'about'" class="absolute left-0 top-full w-full bg-teal-700 shadow-lg z-10 text-left">
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">歷史沿革</a></li>
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">樓層介紹</a></li>
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">醫療團隊</a></li>
            </ul>
          </li>

          <li class="relative flex-1 text-center">
            <button @click="toggleMenu('news')" class="w-full flex justify-center items-center py-4 px-3 hover:bg-teal-700 transition-colors duration-200">
              <span>最新消息</span>
              <svg class="w-4 h-4 ml-1.5 transition-transform duration-300" :class="{ 'rotate-180': openMenuKey === 'news' }" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </button>
            <ul v-if="openMenuKey === 'news'" class="absolute left-0 top-full w-full bg-teal-700 shadow-lg z-10 text-left">
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">院內公告</a></li>
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">媒體報導</a></li>
            </ul>
          </li>

          <li class="relative flex-1 text-center">
            <button @click="toggleMenu('recruitment')" class="w-full flex justify-center items-center py-4 px-3 hover:bg-teal-700 transition-colors duration-200">
              <span>徵才資訊</span>
              <svg class="w-4 h-4 ml-1.5 transition-transform duration-300" :class="{ 'rotate-180': openMenuKey === 'recruitment' }" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
            </button>
            <ul v-if="openMenuKey === 'recruitment'" class="absolute left-0 top-full w-full bg-teal-700 shadow-lg z-10 text-left">
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">職位列表</a></li>
              <li><a href="#" class="block px-4 py-2 hover:bg-teal-800 transition-colors">應徵方式</a></li>
            </ul>
          </li>

        </ul>
      </div>
    </nav>

  </header>
</template>

<style scoped>

</style>