<template>
  <main class="font-sans">

    <section class="container mx-auto py-20 sm:px-6">
      <div class="grid grid-cols-2 lg:grid-cols-100 gap-8">
        <div class="bg-gray-100 rounded-lg p-6 shadow-lg border-l-4 border-teal-500">
          <h2 class="text-2xl font-bold text-teal-700 mb-4">掛號須知</h2>
          <div>
            <ul class="list-disc list-inside text-gray-700 space-y-1 mb-4">
              <li>請攜帶身分證或健保卡。</li>
              <li>至一樓櫃檯填寫初診基本資料表。</li>
              <li>完成後至掛號櫃檯辦理掛號。</li>
            </ul>
            <p class="mt-4 text-sm text-gray-500">
              初診請至一樓大廳，填寫基本資料再行看診
            </p>
          </div>
        </div>
        <div class="shadow-lg p-10 mx-auto">
            <h4>復健科 王醫師看診號碼</h4>
            <p class="text-5xl p-7 text-center">20</p>
        </div>
      </div>
    </section>

    <section class="container mx-auto py-6 sm:px-6">
      <div class="bg-white rounded-lg p-6 shadow-lg border-l-4 border-red-500">
        <h2 class="text-2xl font-bold text-red-700 mb-4">醫院公告</h2>
        <div>
          <ul class="space-y-3 text-gray-800">
            <li class="border-b pb-2">
              <a href="#" class="hover:text-red-600 transition-colors">
                <span class="text-sm text-gray-500 block">2025-08-26</span>
                颱風來襲，本院門診時間調整通知
              </a>
            </li>
            <li class="border-b pb-2">
              <a href="#" class="hover:text-red-600 transition-colors">
                <span class="text-sm text-gray-500 block">2025-08-22</span>
                流感疫苗開始施打，請洽詢家醫科門診
              </a>
            </li>
            <li>
              <a href="#" class="hover:text-red-600 transition-colors">
                <span class="text-sm text-gray-500 block">2025-08-15</span>
                新增夜間復健門診服務時間
              </a>
            </li>
          </ul>
          <a href="#" class="text-teal-600 hover:underline font-medium mt-4 inline-block">查看更多公告...</a>
        </div>
      </div>
    </section>

    <section class="bg-gray-100 py-12">
      <div class="container mx-auto px-4 sm:px-6">
        <h2 class="text-3xl font-bold text-center text-teal-700 mb-10">醫院環境巡禮</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300">
            <img src="/images/contentA.jpg" alt="醫院環境照片 1" class="w-full h-56 object-cover">
          </div>
          <div class="rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300">
            <img src="/images/contentB.jpg" alt="醫院環境照片 2" class="w-full h-56 object-cover">
          </div>
          <div class="rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300">
            <img src="/images/contentC.jpg" alt="醫院環境照片 3" class="w-full h-56 object-cover">
          </div>
        </div>
          <p class="mt-10 text-center text-gray-600 shadow-sm  shadow-yellow-300/70 p-10 bg-gray-50 rounded-lg max-w-2xl mx-auto">舒適明亮的環境，提供您安心的就醫體驗。</p>
      </div>
    </section>
  </main>
</template>

<script setup>
// 這個元件目前不需要任何 JavaScript 邏輯
</script>

<style scoped>
/* 如果您需要針對這個元件寫一些特定的 CSS，可以寫在這裡 */
/* 例如： */
.aspect-w-16 {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
}
.aspect-h-9 > * {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
}
</style>