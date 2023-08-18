<template>
  <nav class="border-b bg-white top-0 left-0 w-full fixed z-10">
    <div class="flex flex-col md:flex-row items-center justify-between w-full px-4 mx-auto">
      <div class="flex-1 items-center flex-grow">
      </div>
      <div class="flex-2 items-center justify-center flex-grow my-2">
        <h1 class="text-4xl font-bold text-center">{{ title }}</h1>
      </div>
      <div class="flex-1 items-center flex-grow">
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">

defineProps({
  title: String,
})
</script>