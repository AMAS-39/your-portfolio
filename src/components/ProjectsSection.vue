<template>
  <section id="projects" class="bg-background text-white py-20 px-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl sm:text-5xl font-bold text-primary mb-12 text-center">My Projects</h2>

      <!-- Featured AI & Research Projects -->
      <div class="mb-16" data-aos="fade-up">
        <h3 class="text-2xl font-semibold text-cyan-400 mb-8 flex items-center gap-3">
          <span class="text-3xl">🚀</span> Featured AI & Research Projects
        </h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div
            v-for="(project, index) in featuredProjects"
            :key="index"
            class="bg-gray-800 rounded-xl overflow-hidden shadow-lg hover:shadow-xl hover:-translate-y-1 transition-transform duration-300 border-l-4 border-cyan-400"
          >
            <div class="p-6 flex flex-col h-full">
              <h3 class="text-xl font-semibold mb-2 text-primary">{{ project.title }}</h3>
              <p class="text-gray-300 text-sm flex-1 mb-3">{{ project.description }}</p>
              
              <p v-if="project.impact" class="text-gray-400 text-xs italic mb-3">
                <span class="text-primary font-medium">Impact:</span> {{ project.impact }}
              </p>
              
              <div class="mt-auto">
                <div class="flex flex-wrap gap-2 mb-4">
                  <span
                    v-for="tag in project.tags"
                    :key="tag"
                    class="text-xs px-3 py-1 bg-cyan-900/50 text-cyan-300 rounded-full border border-cyan-700"
                  >
                    {{ tag }}
                  </span>
                </div>
                <div class="flex gap-2 justify-start flex-wrap">
                  <a
                    v-if="project.live"
                    :href="project.live"
                    target="_blank"
                    class="px-4 py-2 rounded-lg bg-primary text-black font-medium hover:bg-white transition text-sm"
                  >
                    Live
                  </a>
                  <a
                    v-if="project.github"
                    :href="project.github"
                    target="_blank"
                    class="px-4 py-2 rounded-lg border border-primary text-primary hover:bg-primary hover:text-black transition text-sm"
                  >
                    GitHub
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Production & Client Systems -->
      <div class="mb-16" data-aos="fade-up">
        <h3 class="text-2xl font-semibold text-cyan-400 mb-8 flex items-center gap-3">
          <span class="text-3xl">💼</span> Production & Client Systems
        </h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div
            v-for="(project, index) in productionProjects"
            :key="index"
            class="bg-gray-800 rounded-xl overflow-hidden shadow-lg hover:shadow-xl hover:-translate-y-1 transition-transform duration-300"
          >
            <div class="p-6 flex flex-col h-full">
              <h3 class="text-xl font-semibold mb-2 text-primary">{{ project.title }}</h3>
              <p class="text-gray-300 text-sm flex-1 mb-3">{{ project.description }}</p>
              
              <p v-if="project.impact" class="text-gray-400 text-xs italic mb-3">
                <span class="text-primary font-medium">Impact:</span> {{ project.impact }}
              </p>
              
              <div class="mt-auto">
                <div class="flex flex-wrap gap-2 mb-4">
                  <span
                    v-for="tag in project.tags"
                    :key="tag"
                    class="text-xs px-3 py-1 bg-gray-700 text-gray-200 rounded-full"
                  >
                    {{ tag }}
                  </span>
                </div>
                <div class="flex gap-2 justify-start flex-wrap">
                  <a
                    v-if="project.live"
                    :href="project.live"
                    target="_blank"
                    class="px-4 py-2 rounded-lg bg-primary text-black font-medium hover:bg-white transition text-sm"
                  >
                    Live
                  </a>
                  <a
                    v-if="project.github"
                    :href="project.github"
                    target="_blank"
                    class="px-4 py-2 rounded-lg border border-primary text-primary hover:bg-primary hover:text-black transition text-sm"
                  >
                    GitHub
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Systems, Platforms & Web -->
      <div class="mb-16" data-aos="fade-up">
        <h3 class="text-2xl font-semibold text-cyan-400 mb-8 flex items-center gap-3">
          <span class="text-3xl">⚙️</span> Systems, Platforms & Web
        </h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div
            v-for="(project, index) in systemsProjects"
            :key="index"
            class="bg-gray-800 rounded-xl overflow-hidden shadow-lg hover:shadow-xl hover:-translate-y-1 transition-transform duration-300"
          >
            <div class="p-6 flex flex-col h-full">
              <h3 class="text-xl font-semibold mb-2 text-primary">{{ project.title }}</h3>
              <p class="text-gray-300 text-sm flex-1 mb-3">{{ project.description }}</p>
              
              <p v-if="project.impact" class="text-gray-400 text-xs italic mb-3">
                <span class="text-primary font-medium">Impact:</span> {{ project.impact }}
              </p>
              
              <div class="mt-auto">
                <div class="flex flex-wrap gap-2 mb-4">
                  <span
                    v-for="tag in project.tags"
                    :key="tag"
                    class="text-xs px-3 py-1 bg-gray-700 text-gray-200 rounded-full"
                  >
                    {{ tag }}
                  </span>
                </div>
                <div class="flex gap-2 justify-start flex-wrap">
                  <a
                    v-if="project.live"
                    :href="project.live"
                    target="_blank"
                    class="px-4 py-2 rounded-lg bg-primary text-black font-medium hover:bg-white transition text-sm"
                  >
                    Live
                  </a>
                  <a
                    v-if="project.github"
                    :href="project.github"
                    target="_blank"
                    class="px-4 py-2 rounded-lg border border-primary text-primary hover:bg-primary hover:text-black transition text-sm"
                  >
                    GitHub
                  </a>
                  <button
                    v-if="project.images"
                    @click="openModal(project)"
                    class="px-4 py-2 rounded-lg border border-gray-400 text-gray-300 hover:bg-gray-700 transition text-sm"
                  >
                    View Images
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Events / Impact Work -->
      <div data-aos="fade-up">
        <h3 class="text-2xl font-semibold text-cyan-400 mb-8 flex items-center gap-3">
          <span class="text-3xl">🌟</span> Events / Impact Work
        </h3>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div
            v-for="(project, index) in impactWork"
            :key="index"
            class="bg-gray-800 rounded-xl overflow-hidden shadow-lg hover:shadow-xl hover:-translate-y-1 transition-transform duration-300 border-l-4 border-yellow-500"
          >
            <div class="p-6 flex flex-col h-full">
              <h3 class="text-xl font-semibold mb-2 text-primary">{{ project.title }}</h3>
              <p class="text-gray-300 text-sm flex-1 mb-3">{{ project.description }}</p>
              
              <p v-if="project.impact" class="text-gray-400 text-xs italic mb-3">
                <span class="text-primary font-medium">Impact:</span> {{ project.impact }}
              </p>
              
              <div class="mt-auto">
                <div class="flex flex-wrap gap-2 mb-4">
                  <span
                    v-for="tag in project.tags"
                    :key="tag"
                    class="text-xs px-3 py-1 bg-yellow-900/50 text-yellow-300 rounded-full border border-yellow-700"
                  >
                    {{ tag }}
                  </span>
                </div>
                <div class="flex gap-2 justify-start flex-wrap">
                  <a
                    v-if="project.live"
                    :href="project.live"
                    target="_blank"
                    class="px-4 py-2 rounded-lg bg-primary text-black font-medium hover:bg-white transition text-sm"
                  >
                    Live
                  </a>
                  <a
                    v-if="project.github"
                    :href="project.github"
                    target="_blank"
                    class="px-4 py-2 rounded-lg border border-primary text-primary hover:bg-primary hover:text-black transition text-sm"
                  >
                    GitHub
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Modal -->
    <div
      v-if="showModal"
      class="fixed inset-0 z-50 bg-black bg-opacity-80 flex items-center justify-center px-4"
    >
      <div class="bg-gray-900 max-w-3xl w-full rounded-lg overflow-hidden shadow-lg relative">
        <div class="flex justify-between items-center p-4 border-b border-gray-700">
          <h3 class="text-lg font-semibold text-primary">{{ activeTitle }}</h3>
          <button @click="showModal = false" class="text-white hover:text-red-400 text-2xl">&times;</button>
        </div>
        <div class="p-4 grid grid-cols-1 sm:grid-cols-2 gap-4 max-h-[70vh] overflow-y-auto">
          <img
            v-for="(img, i) in activeImages"
            :key="i"
            :src="img"
            alt="Project Screenshot"
            class="rounded shadow-lg border border-gray-700"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const showModal = ref(false)
const activeImages = ref([])
const activeTitle = ref('')

const openModal = (project) => {
  activeImages.value = project.images || []
  activeTitle.value = project.title
  showModal.value = true
}

const featuredProjects = [
  {
    title: 'Let Me Pass – AI Parking Communication System',
    description:
      'Flutter application with YOLOv8-based license plate recognition, real-time driver chat, and optimized notification workflows.',
    tags: ['Flutter', 'YOLOv8', 'Computer Vision', 'Real-time'],
    impact: 'faster parking conflict resolution',
    live: '',
    github: '',
  },
  {
    title: 'CAMK – Kurdish Academic Social Platform',
    description:
      'Cross-platform academic platform built with Vue.js, Laravel, and Flutter, promoting Kurdish digital content for AI training and education.',
    tags: ['Vue.js', 'Laravel', 'Flutter', 'Kurdish AI Data'],
    live: '',
    github: '',
  },
  {
    title: 'TIU AI Chatbot',
    description:
      'Multilingual chatbot (Kurdish, Arabic, English) developed for the Computer Education Department at TIU.',
    tags: ['NLP', 'Multilingual', 'Chatbot'],
    live: '',
    github: '',
  },
]

const productionProjects = [
  {
    title: 'MasterMind Jobs',
    description:
      'Cross-platform job marketplace (iOS & Android) featuring AI-driven recommendations, real-time chat, and company dashboards; published on App Store and Google Play.',
    tags: ['Flutter', 'Firebase', 'Flask', 'AI'],
    impact: 'job matching + real-time communication',
    live: '',
    github: '',
  },
  {
    title: 'Cars Colosseum Platform',
    description:
      'End-to-end development of a mobile application and backend system for locating second-hand car parts and service centers across Kurdistan.',
    tags: ['React Native', 'Laravel', 'Mobile', 'APIs'],
    live: '',
    github: '',
  },
  {
    title: 'Logistics Applications',
    description:
      'Contributed to multiple logistics-focused mobile applications supporting operational tracking and delivery workflows (Kosto Log, Ramze Bazzaz, China Stars Log).',
    tags: ['Flutter', 'Logistics', 'Tracking'],
    live: '',
    github: '',
  },
  {
    title: 'Nice Village App – Backend',
    description:
      'Backend development and API integration for a Flutter application with real-time data and authentication.',
    tags: ['Flask', 'Firebase', 'REST API', 'Auth'],
    live: '',
    github: '',
  },
]

const systemsProjects = [
  {
    title: 'S4YMS – Soft4U Internal Developer System',
    description:
      'Part of the core team developing an internal management system for developers, supporting workflow organization and technical operations.',
    tags: ['Internal System', 'Workflow'],
    live: '',
    github: '',
  },
  {
    title: 'KKYO Website & Admin Panel',
    description:
      'Designed and developed the official KKYO website and admin system, improving coordination among departments.',
    tags: ['Vue.js', 'Flask', 'Admin Panel'],
    impact: 'improved coordination across departments',
    live: 'https://www.kkyo.org',
    github: 'https://github.com/AMAS-39/kkyo-website',
  },
  {
    title: 'Gym Management System',
    description:
      'Full gym management system with Admin, Trainer, and User dashboards, workout scheduling, and progress tracking.',
    tags: ['Laravel', 'Dashboards', 'Scheduling'],
    images: ['src/assets/images/home.png', 'src/assets/images/login.png'],
    live: '',
    github: '',
  },
  {
    title: 'Multi-Language Dynamic Menu Builder',
    description:
      'Restaurant menu system supporting Kurdish, Arabic, and English.',
    tags: ['Laravel', 'Localization', 'Multilingual'],
    live: '',
    github: '',
  },
  {
    title: 'Cactus RIE Website',
    description:
      'Developed the front-end using Vue.js, focusing on clean UI and responsive design.',
    tags: ['Vue.js', 'Responsive UI'],
    live: '',
    github: '',
  },
  {
    title: 'Halabja Memorial Website',
    description:
      'Memorial website featuring historical content and an interactive 3D monument view.',
    tags: ['Web', '3D', 'Interactive'],
    live: '',
    github: '',
  },
]

const impactWork = [
  {
    title: 'Korea Week Festival 2025 – IT Support Manager',
    description:
      'Led IT operations and implemented a QR-based registration system for a two-day international festival (TIU & Korean Consulate, Erbil).',
    tags: ['QR System', 'Event IT', 'Operations'],
    live: '',
    github: '',
  },
]
</script>


<style scoped>
</style>
