<template>
  <section id="projects" class="bg-background text-white py-20 px-6">
    <div class="max-w-6xl mx-auto text-center">
      <h2 class="text-4xl sm:text-5xl font-bold text-primary mb-12">My Projects</h2>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="bg-gray-800 rounded-xl overflow-hidden shadow-md hover:shadow-xl hover:-translate-y-1 transition-transform duration-300"
        >
          <div class="p-6 flex flex-col h-full">
            <h3 class="text-2xl font-semibold mb-2 text-primary">{{ project.title }}</h3>
            <p class="text-gray-300 text-sm flex-1">{{ project.description }}</p>

            <div class="mt-4 flex flex-wrap gap-2">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="text-xs px-3 py-1 bg-gray-700 text-gray-200 rounded-full"
              >
                {{ tag }}
              </span>
            </div>

            <div class="mt-6 flex gap-4 justify-center flex-wrap">
              <a
                v-if="project.live"
                :href="project.live"
                target="_blank"
                class="px-4 py-2 rounded-lg bg-primary text-black font-medium hover:bg-white transition"
              >
                Live
              </a>
              <a
                v-if="project.github"
                :href="project.github"
                target="_blank"
                class="px-4 py-2 rounded-lg border border-primary text-primary hover:bg-primary hover:text-black transition"
              >
                GitHub
              </a>
              <button
                v-if="project.images"
                @click="openModal(project)"
                class="px-4 py-2 rounded-lg border border-gray-400 text-gray-300 hover:bg-gray-700 transition"
              >
                View Images
              </button>
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

const projects = [
  {
    title: 'TIU AI Chatbot',
    description: 'Multilingual chatbot (Kurdish, English, Arabic) to assist Computer Education Department at TIU.',
    tags: ['Vue.js', 'NLP', 'OpenAI', 'Flask'],
    github: '',
    live: '',
  },
  {
    title: 'Chemk – Academic Platform',
    description: 'Kurdish academic social platform built using Vue, Laravel, and Flutter.',
    tags: ['Vue.js', 'Laravel', 'Flutter'],
    github: '',
    live: '',
  },
  {
    title: 'KKYO Volunteer System',
    description: 'Volunteer management system with department heads, point tracking, and structured roles.',
    tags: ['Laravel', 'Admin Panel'],
    github: 'https://github.com/AMAS-39/kkyo_volunteer_system',
    live: '',
  },
  {
    title: 'Let Me Pass – AI Access System',
    description: 'AI-based secure access system using face detection and automation, presented at ICASEE 2025.',
    tags: ['Python', 'OpenCV', 'AI'],
    github: '',
    live: '',
  },
  {
    title: 'MemoryMate AI',
    description: 'Alzheimer assistant with activity tracking, live location, voice assistant, and caregiver dashboard.',
    tags: ['Flutter', 'AI', 'Firebase'],
    github: '',
    live: '',
  },
  {
    title: 'Menu Builder (Multilingual)',
    description: 'Lightning-fast restaurant menu builder supporting Kurdish, Arabic, and English using Laravel.',
    tags: ['Laravel', 'Localization'],
    github: '',
    live: '',
  },
  {
    title: 'KKYO Website & Admin Panel',
    description: 'Built the full website and admin dashboard for KKYO to manage events and members. Improved coordination between department heads.',
    tags: ['Vue.js', 'Flask', 'Admin'],
    github: 'https://github.com/AMAS-39/kkyo-website',
    live: 'https://www.kkyo.org',
  },
  {
    title: 'Nice Village App – Backend',
    description: 'Created Flask + Firebase backend for a real-time app with authentication and performance APIs.',
    tags: ['Flask', 'Firebase'],
    github: '',
    live: '',
  },
  {
    title: 'Dynamic Menu UI – Vue.js',
    description: 'Frontend UI for the menu builder with real-time responsiveness using Vue and Tailwind.',
    tags: ['Vue.js', 'Tailwind CSS'],
    github: '',
    live: '',
  },
  {
    title: 'Halabja Memorial Website',
    description: 'Developed a historical site for Halabja’s memory with 3D monument exploration.',
    tags: ['3D View', 'Vue.js'],
    github: 'https://github.com/AMAS-39/halabja-memorial',
    live: 'https://amas-39.github.io/halabja-memorial/?fbclid=IwY2xjawKubZVleHRuA2FlbQIxMABicmlkETFFdFVSS2NjQ2xLYzltMU15AR7tmtFraVHZv7eDMckO0DPDXZj5Qabo0tikqWn3bz6mp1VzKHTlO5uZx1SndQ_aem_8bcD4gO-5PgEOCvx_G5ODA',
  },
  {
    title: 'Gym Management System',
    description: 'Admin, Trainer, and User dashboards, workout scheduler, and progress tracker built with Laravel.',
    tags: ['Laravel', 'Dashboard'],
    github: 'https://github.com/AMAS-39/gym-management',
    live: '',
    images: ['src/assets/images/home.png', 'src/assets/images/login.png']
  }
]
</script>


<style scoped>
</style>
