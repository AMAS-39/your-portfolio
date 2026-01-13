<template>
  <header class="fixed top-0 left-0 w-full z-50 bg-background/90 backdrop-blur shadow-md">
    <nav class="max-w-6xl mx-auto px-4 sm:px-6 py-4 flex justify-between items-center">
      <!-- ✅ Logo -->
<h1 class="text-xl sm:text-2xl font-bold text-primary">
  ahmad<span class="text-cyan-400">code.tech</span>
</h1>

      <!-- ✅ Desktop Nav -->
      <ul class="hidden md:flex gap-6 text-white font-medium">
        <li><a href="#projects" class="hover:text-primary transition">Projects</a></li>
        <li><a href="#research" class="hover:text-primary transition">Research</a></li>
        <li><a href="#experience" class="hover:text-primary transition">Experience</a></li>
        <li><a href="#leadership" class="hover:text-primary transition">Leadership</a></li>
        <li><a href="#skills" class="hover:text-primary transition">Skills</a></li>
        <li><a href="#about" class="hover:text-primary transition">About</a></li>
        <li><a href="#contact" class="hover:text-primary transition">Contact</a></li>
      </ul>

      <!-- ✅ Mobile Toggle -->
      <button
        class="md:hidden text-white text-sm focus:outline-none"
        @click="toggleMenu"
        aria-label="Toggle menu"
      >
        <i :class="menuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
      </button>
    </nav>

    <!-- ✅ Mobile Menu -->
    <transition name="fade">
      <div
        v-if="menuOpen"
        class="md:hidden bg-background/90 backdrop-blur px-6 pb-6 pt-4 text-center text-white font-medium space-y-4 shadow-md"
      >
        <a href="#projects" class="block hover:text-primary" @click="closeMenu">Projects</a>
        <a href="#research" class="block hover:text-primary" @click="closeMenu">Research</a>
        <a href="#experience" class="block hover:text-primary" @click="closeMenu">Experience</a>
        <a href="#leadership" class="block hover:text-primary" @click="closeMenu">Leadership</a>
        <a href="#skills" class="block hover:text-primary" @click="closeMenu">Skills</a>
        <a href="#about" class="block hover:text-primary" @click="closeMenu">About</a>
        <a href="#contact" class="block hover:text-primary" @click="closeMenu">Contact</a>
      </div>
    </transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
