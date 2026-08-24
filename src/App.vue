<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from '@/components/NavBar.vue'
</script>

<template>
  <div class="min-h-screen bg-background">
    <NavBar />
    <main class="pt-8 px-6">
      <RouterView />

    </main>
  </div>
</template>
