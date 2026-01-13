<template>
  <section class="bg-gray-900 text-white py-16 px-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl sm:text-4xl font-bold text-primary mb-12 text-center">What I Build</h2>
      
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(item, index) in buildItems"
          :key="index"
          class="bg-gray-800 rounded-lg p-6 shadow-lg hover:shadow-xl hover:-translate-y-1 transition duration-300 text-center"
          data-aos="fade-up"
          :data-aos-delay="index * 100"
        >
          <div class="text-4xl mb-4">{{ item.icon }}</div>
          <p class="text-gray-300 font-medium">{{ item.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const buildItems = [
  { icon: '🤖', text: 'AI-powered mobile applications' },
  { icon: '📱', text: 'Real-time Flutter systems' },
  { icon: '🌐', text: 'Multilingual & Kurdish-focused platforms' },
  { icon: '🔒', text: 'Secure APIs with Flask & Laravel' },
  { icon: '👁️', text: 'Computer vision & NLP solutions' },
]
</script>

<style scoped>
</style>
