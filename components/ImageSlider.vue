<script setup>
import { ref } from 'vue';

// 1. 引入 Swiper 元件和 CSS
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

// 2. 引入您需要的功能模組
import { Navigation, Pagination, Autoplay } from 'swiper/modules';

// 準備要輪播的圖片資料 (使用 public 資料夾的路徑)
const items = ref([
  '/images/c1.jpg',
  '/images/c2.jpg',
  '/images/c3.jpg',
]);

// 將模組綁定到一個變數
const modules = [Navigation, Pagination, Autoplay];
</script>

<template>
  <div class="py-8">
    <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="30"
        :loop="true"
        :pagination="{ clickable: true }"
        :navigation="true"
        :autoplay="{
        delay: 2500,
        disableOnInteraction: false,
      }"
        class="rounded-lg"
    >
      <swiper-slide v-for="item in items" :key="item">
        <img :src="item" class="w-full h-auto object-cover" alt="輪播圖片" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<style>
/* 這裡是 Swiper 自訂樣式的部分
  可以用來覆蓋預設的顏色
*/
.swiper-button-next,
.swiper-button-prev {
  color: white; /* 將左右箭頭設為白色 */
}

.swiper-pagination-bullet-active {
  background: white; /* 將當前分頁圓點設為白色 */
}
</style>