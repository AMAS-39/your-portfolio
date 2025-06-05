<template>
  <section id="academics" class="bg-background text-white py-20 px-6">
    <div class="max-w-4xl mx-auto">
      <h2 class="text-4xl sm:text-5xl font-bold text-primary text-center mb-12">Academic Contributions</h2>

      <!-- Filter -->
      <div class="flex flex-wrap justify-center gap-4 mb-10">
        <button
          v-for="year in years"
          :key="year"
          @click="activeYear = year"
          class="px-4 py-1 rounded-full border border-primary text-sm hover:bg-primary hover:text-black transition"
          :class="{ 'bg-primary text-black': activeYear === year }"
        >
          {{ year }}
        </button>
      </div>

      <div class="border-l-4 border-primary pl-6 space-y-10 relative">
        <div
          v-for="(event, index) in filteredEvents"
          :key="index"
          class="relative"
          data-aos="fade-up"
        >
          <div class="absolute -left-3 top-0 w-6 h-6 bg-primary rounded-full border-4 border-background"></div>

          <div class="mb-2 ml-4 flex items-center gap-3">
            <span class="text-sm uppercase tracking-wide text-gray-400">{{ event.date }}</span>
          </div>
          <h3 class="text-xl font-semibold text-primary">{{ event.title }}</h3>
          <p class="text-gray-300 text-sm">{{ event.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from 'vue'

const activeYear = ref('All')

const events = [
      {
    date: 'May 2025',
    title: 'NAYRIC 2025 – Research Contributor',
    description: 'Research on TIUchatbot and Nozhdar AI Application.',
    year: 2024,
  },
  {
    date: 'May 2025',
    title: 'ICOWOBAS 2025 – Malaysia',
    description: 'Presented two AI projects: Nozhdar and MemoryMate.',
    year: 2025,
  },
  {
    date: 'April 2025',
    title: 'ICASEE 2025 – Erbil',
    description: 'Presented CAMK and Let Me Pass AI projects.',
    year: 2025,
  },
  {
    date: 'Dec 2024',
    title: 'NAYRIC 2024 – Research Contributor',
    description: 'Research on face detection and heritage digitization.',
    year: 2024,
  },
  {
    date: 'April 2024',
    title: 'TIU Spring Festival – 2nd Place',
    description: 'Sign Language Recognition System.',
    year: 2024,
  },
]

const years = ['All', 2025, 2024]

const filteredEvents = computed(() =>
  activeYear.value === 'All'
    ? events
    : events.filter((event) => event.year === activeYear.value)
)
</script>
