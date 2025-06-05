<template>
  <section
    class="relative w-full h-screen flex flex-col justify-center items-center text-center px-4 sm:px-6 lg:px-8 bg-animated overflow-hidden"
  >
    <!-- ✨ Floating Background Dots -->
    <div class="absolute top-10 left-10 w-4 h-4 bg-primary rounded-full animate-ping"></div>
    <div class="absolute bottom-20 right-16 w-3 h-3 bg-cyan-400 rounded-full animate-bounce"></div>

<!-- 🌟 Animated Glowing Image -->
<div class="relative mt-8 sm:mt-0 mb-2 flex justify-center">
  <div class="absolute w-44 h-44 sm:w-52 sm:h-52 rounded-full bg-primary blur-2xl opacity-30 animate-pulse"></div>
  <img
    src="/your-photo.jpg"
    alt="Ahmad Shwan"
    class="relative w-40 h-40 sm:w-48 sm:h-48 rounded-full border-4 border-primary shadow-2xl object-cover hover:scale-105 transition duration-300"
  />
</div>


    <!-- 🌈 Main Content -->
    <div class="z-10 w-full max-w-4xl mx-auto animate-fade-in">
      <div class="px-4 sm:px-10 space-y-4">
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold bg-gradient-to-r from-primary to-cyan-400 text-transparent bg-clip-text leading-tight animate-float">
          Ahmad Shwan
        </h1>

        <h2 class="text-lg sm:text-xl lg:text-2xl font-medium text-white tracking-wide">
          Full-Stack Software Developer
        </h2>

        <!-- ⌨️ Typing Effect -->
        <p class="text-base sm:text-lg text-gray-300 min-h-[2rem] animate-fade-loop">
          <span ref="typedText"></span>
        </p>

        <!-- 🚀 Buttons -->
        <div class="flex flex-wrap justify-center gap-4 pt-4">
          <a
            href="#projects"
            class="px-6 py-3 rounded-lg bg-primary text-black font-semibold hover:bg-white hover:text-black transition shadow-lg"
          >
            View Projects
          </a>
          <a
            href="/AhmadShwan-CV.pdf"
            download
            target="_blank"
            class="px-6 py-3 rounded-lg border border-primary text-primary hover:bg-primary hover:text-black transition shadow-lg"
          >
            Download CV
          </a>
        </div>
      </div>
    </div>


  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'

const typedText = ref(null)

onMounted(() => {
  const typedScript = document.createElement('script')
  typedScript.src = 'https://cdn.jsdelivr.net/npm/typed.js@2.0.12'
  typedScript.onload = () => {
    new window.Typed(typedText.value, {
      strings: [
        'Vue.js Developer',
        'Laravel Developer',
        'Flutter Developer',
        'AI Developer',
        'Independent Researcher',
        'Educator',
      ],
      typeSpeed: 60,
      backSpeed: 30,
      backDelay: 1500,
      loop: true,
    })
  }
  document.body.appendChild(typedScript)
})
</script>

<style scoped>
@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
.animate-fade-in {
  animation: fade-in 1s ease-out;
}

@keyframes fade-loop {
  0%, 100% { opacity: 0.3; }
  50% { opacity: 1; }
}
.animate-fade-loop {
  animation: fade-loop 3s ease-in-out infinite;
}

@keyframes bg-pan {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
.bg-animated {
  background: linear-gradient(270deg, #0f172a, #1e293b, #0f172a);
  background-size: 600% 600%;
  animation: bg-pan 10s ease infinite;
}

@keyframes float {
  0%   { transform: translateY(0); }
  50%  { transform: translateY(-8px); }
  100% { transform: translateY(0); }
}
.animate-float {
  animation: float 4s ease-in-out infinite;
}
</style>
