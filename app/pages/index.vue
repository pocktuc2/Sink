<script setup>
const pageInfo = {
  title: '短網址服務',
  message: '這裡沒有東西'
}
</script>

<template>
  <!-- 不用 NuxtLayout，直接渲染全螢幕 -->
  <main class="min-h-screen flex items-center justify-center px-6">
    <div class="text-center space-y-6 max-w-md mx-auto">
      <!-- 標題 -->
      <h1 class="text-2xl font-medium text-gray-800">
        {{ pageInfo.title }}
      </h1>

      <!-- 描述 -->
      <p class="text-gray-600 leading-relaxed">
        {{ pageInfo.message }}
      </p>
    </div>
  </main>
</template>
