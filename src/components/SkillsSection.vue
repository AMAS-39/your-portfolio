<template>
  <section id="skills" class="min-h-screen bg-background text-white py-20 px-6">
    <div class="max-w-6xl mx-auto text-center">
      <h2 class="text-4xl sm:text-5xl font-bold text-primary mb-12">My Tech Stack</h2>

      <!-- ✅ Responsive Grid Only -->
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-8">
        <a
          v-for="(skill, index) in skills"
          :key="index"
          :href="skill.url"
          target="_blank"
          class="group"
          :data-aos="'fade-up'"
          :data-aos-delay="index * 100"
        >
          <div
            class="flex flex-col items-center justify-center bg-gradient-to-br from-gray-800 to-gray-900 hover:from-gray-700 hover:to-gray-800 rounded-xl p-6 shadow-lg transition-transform duration-300 hover:scale-105 ring-1 ring-gray-700 hover:ring-2 hover:ring-primary"
          >
            <img
              loading="lazy"
              :src="skill.logo"
              :alt="skill.name"
              class="w-16 h-16 mb-4 grayscale group-hover:grayscale-0 transition duration-300"
            />
            <p class="text-lg font-semibold text-white">{{ skill.name }}</p>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
const skills = [
  { name: 'Vue.js', logo: 'https://www.vectorlogo.zone/logos/vuejs/vuejs-icon.svg', url: 'https://vuejs.org/' },
  { name: 'Laravel', logo: 'https://www.vectorlogo.zone/logos/laravel/laravel-icon.svg', url: 'https://laravel.com/' },
  { name: 'Tailwind CSS', logo: 'https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg', url: 'https://tailwindcss.com/' },
  { name: 'Flutter', logo: 'https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg', url: 'https://flutter.dev/' },
  { name: 'Firebase', logo: 'https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg', url: 'https://firebase.google.com/' },
  { name: 'Python', logo: 'https://www.vectorlogo.zone/logos/python/python-icon.svg', url: 'https://python.org/' },
  { name: 'JavaScript', logo: 'https://www.vectorlogo.zone/logos/javascript/javascript-icon.svg', url: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript' },
  { name: 'AI / NLP', logo: 'https://img.icons8.com/color/96/artificial-intelligence.png', url: 'https://en.wikipedia.org/wiki/Natural_language_processing' },
]
</script>

<style scoped>
/* nothing needed */
</style>
