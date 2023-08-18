<template>
  <div class="min-h-screen flex flex-col bg-gray-100">
    <header>
      <TopNav :title="'Mapas de Minecraft'" />
    </header>
    <main class="flex flex-col flex-grow md:justify-center items-center pt-16">
      <h2 class="text-3xl font-bold my-4">Mundos principales</h2>
      <div class="flex flex-col md:flex-row items-center mb-4">
        <Map :emoji="'⛏'" :title="'Survival Comunitario'" :url="'https://mc.wupp.dev/mapas/survival-comunitario'" :bg-image="'./assets/images/survival-vanilla-pve.jpg'" />
        <Map :emoji="'⚡'" :title="'Creativo'" :url="'https://mc.wupp.dev/mapas/creativo'" :bg-image="'./assets/images/creativo-vanilla-parcelas.jpg'" />
        <Map :emoji="'⚔️'" :title="'Survival PvP'" :url="'https://mc.wupp.dev/mapas/survival-pvp'" :bg-image="'./assets/images/survival-vanilla-pvp.jpg'" :enabled="false" />
      </div>
      <h2 class="text-3xl font-bold my-4">Archivo de mundos</h2>
      <div class="flex flex-col md:flex-row items-center mb-4">
        <Map emoji="📗" title="Survival" url="https://mc.wupp.dev/mapas/archivo/survival" bgImage="./assets/images/legacy-survival.jpg" />
        <Map emoji="📘" title="Creativo" url="https://mc.wupp.dev/mapas/archivo/creativo" bgImage="./assets/images/legacy-creativo.jpg" />
        <Map emoji="📕" title="Survival Mamadísimo" url="https://mc.wupp.dev/mapas/archivo/survival-mamadisimo" bgImage="./assets/images/legacy-survival-mamadisimo.jpg" />
      </div>
    </main>
    <Footer />
  </div>
</template>


<script setup lang="ts">
import TopNav from '@/components/TopNav.vue'
import Footer from '@/components/Footer.vue'
import Map from '@/components/Map.vue'

</script>

<style>
.bg-image {
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
</style>
