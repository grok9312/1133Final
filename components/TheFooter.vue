<script setup lang="ts">

</script>

<template>
  <footer class="  bg-gray-800 text-gray-300 font-sans">
    <div class="container mx-auto py-12 px-6">
      <div class="grid grid-cols-1 md:grid-cols-2">
        <div class="space-y-4">
          <h3 class="text-lg font-bold text-white">臺中市立老人復健綜合醫院</h3>
          <ul class="space-y-2">
            <li class="flex items-start">
              <span class="mt-1 mr-2">📍</span>
              <span>地址：407 臺中市西屯區台灣大道四段962號</span>
            </li>
            <li class="flex items-center">
              <span class="mr-2">📞</span>
              <span>掛號專線：(04) 1234-5678</span>
            </li>
          </ul>
        </div>

        <div class="space-y-4">
          <h3 class="text-sm font-bold text-white mt-6">服務時間</h3>
          <p class="text-sm">週一至週五：上午 08:00 - 晚間 21:00</p>
          <p class="text-sm">週六：上午 08:00 - 中午 12:00</p>
          <p class="text-sm">週日及國定假日：休診</p>
        </div>

      </div>
    </div>

    <div class="bg-gray-900 py-4 mt-8">
      <div class="container mx-auto text-center text-sm text-gray-400 px-6">
        <p>&copy; {{ new Date().getFullYear() }} 臺中市立老人復健綜合醫院. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>

</style>