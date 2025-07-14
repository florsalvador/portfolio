<template>
  <div :class="darkMode ? 'dark' : ''">
    <div class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-100 min-h-screen">
      <Navbar :darkMode="darkMode" @toggleDark="toggleDark" />
      <main class="max-w-3xl mx-auto px-4 pt-20 space-y-12">
        <section id="about">
          <h1 class="text-3xl font-bold mb-4">Flor Hernandez</h1>
          <p class="font-bold mb-4">Hi! I’m a web developer who loves learning by building.</p>
          <p>Ever since I discovered the world behind websites, I've been driven by curiosity to understand how things work and how to improve them. I enjoy combining logic and creativity, and I thrive in collaborative teams where ideas and clear communication matter.</p>
        </section>
        <hr class="mt-12 border-gray-300 dark:border-gray-700" />

        <section id="work" class="space-y-8">
          <h2 class="text-2xl font-semibold">Work</h2>
          <div class="flex items-start space-x-4">
            <div class="mt-1 text-pink-500">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <circle cx="10" cy="10" r="5" />
              </svg>
            </div>
            <div>
              <p class="font-bold">Front-End Developer</p>
              <p class="font-light text-gray-600 dark:text-gray-400">Kreante (Nov 2024 – Jan 2025)</p>
              <p>Worked on a production logging app for a major Peruvian dairy company.</p>
            </div>
          </div>
          <div class="flex items-start space-x-4">
            <div class="mt-1 text-pink-500">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <circle cx="10" cy="10" r="5" />
              </svg>
            </div>
            <div>
              <p class="font-bold">Ads Quality Rater</p>
              <p class="font-light text-gray-600 dark:text-gray-400">Telus International AI (Jul 2022 – Oct 2024)</p>
              <p>Reviewed Google ads for quality and relevance using internal guidelines.</p>
            </div>
          </div>
          <div class="flex items-start space-x-4">
            <div class="mt-1 text-pink-500">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <circle cx="10" cy="10" r="5" />
              </svg>
            </div>
            <div>
              <p class="font-bold">Affiliate Marketer & Web Creator</p>
              <p class="font-light text-gray-600 dark:text-gray-400">Freelance (Feb 2012 – Apr 2017)</p>
              <p>Built and customized WordPress sites to promote affiliate offers.</p>
            </div>
          </div>
        </section>
        <hr class="mt-12 border-gray-300 dark:border-gray-700" />

        <section id="projects" class="space-y-4">
          <h2 class="text-2xl font-semibold">Projects</h2>
          <div>
            <p class="font-bold">Restaurant Order Management App</p>
            <p>Web app built with React and TypeScript. The interface adapts to user roles with dynamic state management. Includes login with credential verification and a responsive design optimized for tablets.</p>
          </div>
          <div>
            <p class="font-bold">Fleet Management Software API</p>
            <p>REST API for a taxi company developed with Python and PostgreSQL databases. Implemented multiple endpoints, including user management (CRUD), user authentication with JWT, endpoint protection, and data export to Excel.</p>
          </div>
          <div>
            <p class="font-bold">Movie Catalog App</p>
            <p>Single-page application that fetches movie data from The Movie Database API. Users can browse movies, filter by genre, and sort results by title or popularity.</p>
          </div>
          <div>
            <p class="font-bold">Cat Breeds Chat</p>
            <p>Single-page application developed using vanilla JavaScript and a mobile-first approach. Users can chat with diﬀerent cat breeds using OpenAI's API.</p>
          </div>
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
import { ref } from 'vue';
import Navbar from './components/Navbar.vue';

const darkMode = ref(true);
const toggleDark = () => {
  darkMode.value = !darkMode.value;
};
</script>
