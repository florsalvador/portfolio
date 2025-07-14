<template>
  <header class="fixed top-0 w-full bg-white/70 dark:bg-gray-900/70 backdrop-blur z-50">
    <nav class="max-w-3xl mx-auto flex justify-between items-center px-4 py-3">
      <div class="text-lg font-bold"></div>
      <div class="flex items-center space-x-4">
        <div class="hidden md:flex space-x-6">
          <a href="#work" class="hover:underline">Work</a>
          <a href="#projects" class="hover:underline">Projects</a>
        </div>
        <button @click="handleToggle" class="px-2 py-1">
          <MoonIcon v-if="isDark" class="w-5 h-5"/>
          <SunIcon v-else class="w-5 h-5"/>
          <!-- <component :is="isDark ? MoonIcon : SunIcon" class="w-5 h-5" /> -->
        </button>
        <div class="md:hidden">
          <button @click="open = !open" class="focus:outline-none">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>
    </nav>
    <div v-if="open" class="md:hidden px-4 pb-4">
      <a href="#work" class="block py-2">Work</a>
      <a href="#projects" class="block py-2">Projects</a>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';
import MoonIcon from './MoonIcon.vue';
import SunIcon from './SunIcon.vue';

const open = ref(false);
const isDark = ref(true);
const emit = defineEmits(['toggleDark']);

function handleToggle() {
  isDark.value = !isDark.value
  emit('toggleDark')
}
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
</style>
