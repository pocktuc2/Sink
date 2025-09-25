<script setup>
const pageInfo = {
  title: '短網址服務',
  message: '這裡沒有東西'
}
</script>

<template>

  <main class="min-h-screen flex items-center justify-center px-6">
    <div class="text-center space-y-6 max-w-md mx-auto">

      <h1 class="text-2xl font-medium text-gray-800">
        {{ pageInfo.title }}
      </h1>

      <p class="text-gray-600 leading-relaxed">
        {{ pageInfo.message }}
      </p>
    </div>
  </main>
</template>

<style>
html, body {
  overflow: hidden;
}

section.md\:pt-6 {
  display: none;
}
section.pb-6 {
  display: none;
}
</style>
