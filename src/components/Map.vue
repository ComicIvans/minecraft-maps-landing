<template>
  <div class="text-white bg-white rounded-lg shadow-md p-6 flex flex-col items-center hover:scale-105 transition-transform duration-300 w-64 m-4" :style="{ backgroundImage: 'url(' + bgImage + ')', backgroundSize: 'cover', backgroundPosition: 'center' }">
    <div class="rounded-full bg-gray-200 w-24 h-24 flex items-center justify-center mb-4">
      <span class="text-4xl">{{ emoji }}</span>
    </div>
    <h2 class="text-xl font-bold mb-2 text-center">{{ title }}</h2>
    <a v-if="enabled" :href="url" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded-full">Ver mapa</a>
    <a v-else href="#" class="bg-red-500 hover:bg-red-600 text-white font-bold py-2 px-4 rounded-full">Aun no disponible</a>
  </div>
</template>

<script setup lang="ts">

const props = defineProps({
  emoji: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  url: {
    type: String,
    required: true
  },
  bgImage: {
    type: String,
    required: true
  },
  enabled: {
    type: Boolean,
    default: true
  }
})

</script>