<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <header class="sticky top-0 z-50 w-full border-b border-border/40 bg-background/80 backdrop-blur-md">
    <div class="container mx-auto flex h-16 max-w-7xl items-center justify-between px-6">
      <div class="flex items-center gap-8">
        <RouterLink 
          to="/" 
          class="flex items-center gap-2 font-bold text-lg tracking-tight text-foreground transition-opacity hover:opacity-80"
        >
          <div class="flex h-8 w-8 items-center justify-center rounded-lg bg-primary text-primary-foreground font-extrabold text-sm">
            V
          </div>
          <span>Vue App</span>
        </RouterLink>

        <nav class="flex items-center gap-1 sm:gap-2">
          <RouterLink
            to="/"
            class="rounded-md px-3.5 py-2 text-sm font-medium text-muted-foreground transition-all duration-150 hover:bg-accent hover:text-accent-foreground"
            active-class="!bg-accent !text-accent-foreground font-semibold"
          >
            Home
          </RouterLink>
          <RouterLink
            to="/todo"
            class="rounded-md px-3.5 py-2 text-sm font-medium text-muted-foreground transition-all duration-150 hover:bg-accent hover:text-accent-foreground"
            active-class="!bg-accent !text-accent-foreground font-semibold"
          >
            Todo List
          </RouterLink>
        </nav>
      </div>
    </div>
  </header>
</template>
