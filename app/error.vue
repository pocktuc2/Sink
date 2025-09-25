<script setup>
const props = defineProps({
  error: {
    type: Object,
    default: () => ({ statusCode: 404 })
  }
})

const errorMessages = {
  404: {
    title: '頁面不存在',
    message: '抱歉，您訪問的頁面不存在'
  },
  500: {
    title: '伺服器錯誤',
    message: '伺服器發生錯誤，請稍後再試'
  },
  default: {
    title: '發生錯誤',
    message: '抱歉，發生了未知錯誤'
  }
}

const currentError = errorMessages[props.error.statusCode] || errorMessages.default
</script>

<template>
  <NuxtLayout name="default">
    <div class="error-page min-h-screen flex items-center justify-center px-6">
      <div class="text-center space-y-6 max-w-md mx-auto">
        <!-- 錯誤代碼 -->
        <div class="text-6xl font-light text-gray-300 select-none">
          {{ error.statusCode || '404' }}
        </div>
        
        <!-- 錯誤標題 -->
        <h1 class="text-2xl font-medium text-gray-800">
          {{ currentError.title }}
        </h1>
        
        <!-- 錯誤描述 -->
        <p class="text-gray-600 leading-relaxed">
          {{ currentError.message }}
        </p>
      </div>
    </div>
  </NuxtLayout>
</template>

<style scoped>
.error-page :deep(section.pb-6) {
  display: none;
}
</style>