<template>
  <section
  class="relative w-full h-screen overflow-hidden flex flex-col justify-center items-center text-center px-4 sm:px-6 lg:px-8"
>

    <!-- 🔧 Fullscreen background -->
    <div
      ref="vantaRef"
      class="absolute inset-0 z-0"
      style="pointer-events: none"
    ></div>

    <!-- 🌟 Foreground content -->
   <div class="z-10 w-full max-w-4xl mx-auto animate-fade-in">
      <div class="px-4 sm:px-10">
        <h1
          class="text-3xl sm:text-5xl lg:text-6xl font-bold mb-4 text-primary leading-tight"
        >
          Ahmad Shwan
        </h1>
        <h2
          class="text-lg sm:text-xl lg:text-2xl font-medium text-white mb-4"
        >
          Full-Stack Software Developer
        </h2>

        <!-- Typing Effect -->
        <p class="text-sm sm:text-base md:text-lg text-gray-300 min-h-[2rem] mb-6">
          <span ref="typedText"></span>
        </p>

        <!-- CTA Buttons -->
        <div class="flex flex-wrap justify-center gap-4">
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

    <!-- 🔽 Scroll-down icon -->
    <div class="absolute bottom-6 z-10 animate-bounce text-primary">
      <a href="#skills">
        <i class="fas fa-angle-down text-3xl"></i>
      </a>
    </div>
  </section>
</template>

<script setup>
import { onMounted, onBeforeUnmount, ref } from 'vue'
import * as THREE from 'three'

const vantaRef = ref(null)
const typedText = ref(null)
let vantaEffect = null

onMounted(async () => {
  if (!window.VANTA) {
    const script = document.createElement('script')
    script.src =
      'https://cdn.jsdelivr.net/npm/vanta@latest/dist/vanta.net.min.js'
    script.onload = () => {
      vantaEffect = window.VANTA.NET({
        el: vantaRef.value,
        THREE,
        mouseControls: true,
        touchControls: true,
        minHeight: 200.0,
        minWidth: 200.0,
        scale: 1.0,
        scaleMobile: 1.0,
        color: 0x00ffab,
        backgroundColor: '#0f172a',
      })
    }
    document.body.appendChild(script)
  }

  const typedScript = document.createElement('script')
  typedScript.src = 'https://cdn.jsdelivr.net/npm/typed.js@2.0.12'
  typedScript.onload = () => {
    new window.Typed(typedText.value, {
      strings: [
        'Laravel Developer',
        'Flutter Developer',
        'AI Researcher',
        'UI/UX Engineer',
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

onBeforeUnmount(() => {
  if (vantaEffect) vantaEffect.destroy()
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
</style>
