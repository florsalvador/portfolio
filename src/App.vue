<template>
  <div :class="darkMode ? 'dark' : ''">
    <div class="bg-white dark:bg-gray-900 text-gray-900 dark:text-white min-h-screen">
      <Navbar :darkMode="darkMode" @toggleDark="toggleDark" />
      <main class="max-w-3xl mx-auto px-4 pt-20 space-y-32">
        <section id="about">
          <h1 class="text-3xl font-bold mb-4">Flor Hernandez</h1>
          <h2 class="text-2xl font-semibold mb-4">Web Developer</h2>
          <p>Hi! I’m a web developer who loves learning by building.</p>
          <p>Ever since I discovered the world behind websites, I've been driven by curiosity to understand how things work and how to improve them. I enjoy combining logic and creativity, and I thrive in collaborative teams where ideas and clear communication matter.</p>
          <!-- <p>Ever since I discovered the world behind websites, I've been driven by a curiosity to understand how things work and how to make them better. I'm a creative person who enjoys learning by doing and finding balance between logic and design. I feel most at home in teams that value clear communication, fresh ideas, and thoughtful work.</p> -->
        </section>

        <section id="work">
          <h2 class="text-2xl font-semibold mb-4">Work</h2>
          <p>Work</p>
        </section>

        <section id="projects">
          <h2 class="text-2xl font-semibold mb-4">Projects</h2>
          <p>Projects</p>
        </section>
      </main>

      <footer class="mt-20 py-6 border-t border-gray-200 dark:border-gray-700 text-center">
        <div class="flex justify-center space-x-4">
          <a href="https://www.linkedin.com/in/florhsalvador/" class="hover:underline">LinkedIn</a>
          <a href="https://github.com/florsalvador" class="hover:underline">GitHub</a>
        </div>
      </footer>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Navbar from './components/Navbar.vue'

const darkMode = ref(true);
const toggleDark = () => {
  darkMode.value = !darkMode.value;
};
</script>
