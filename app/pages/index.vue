<script setup>
const errorMessages = {
  empty: {
    title: '短網址服務',
    message: '這裡沒有東西'
  }
}

const currentError = errorMessages.empty
</script>

<template>
  <NuxtLayout name="default">
    <div class="shorturl-page min-h-screen flex items-center justify-center px-6">
      <div class="text-center space-y-6 max-w-md mx-auto">
        <!-- 圖示/分隔線 -->
        <div class="text-6xl font-light text-gray-300 select-none">
          🔗
        </div>

        <!-- 標題 -->
        <h1 class="text-2xl font-medium text-gray-800">
          {{ currentError.title }}
        </h1>

        <!-- 描述 -->
        <p class="text-gray-600 leading-relaxed">
          {{ currentError.message }}
        </p>

        <!-- 分隔線 -->
        <div class="flex justify-center">
          <div class="w-12 h-px bg-gray-300"></div>
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>

<style scoped>
.shorturl-page :deep(section.pb-6),
.shorturl-page :deep(section.md\:pt-6) {
  display: none;
}
</style>