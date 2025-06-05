<template>
  <header class="fixed top-0 left-0 w-full z-50 bg-background/90 backdrop-blur shadow-md">
    <nav class="max-w-6xl mx-auto px-4 sm:px-6 py-4 flex justify-between items-center">
      <!-- Logo / Brand -->
      <h1 class="text-xl sm:text-2xl font-bold text-primary">
        Ahmad.dev
      </h1>

      <!-- Desktop Navigation -->
      <ul class="hidden md:flex gap-6 text-white font-medium">
        <li><a href="#skills" class="hover:text-primary transition">Skills</a></li>
        <li><a href="#projects" class="hover:text-primary transition">Projects</a></li>
        <li><a href="#academics" class="hover:text-primary transition">Academics</a></li>
        <li><a href="#about" class="hover:text-primary transition">About</a></li>
        <li><a href="#contact" class="hover:text-primary transition">Contact</a></li>
      </ul>

      <!-- Mobile Menu Toggle -->
      <button class="md:hidden text-white text-2xl" @click="toggleMenu">
        <i :class="menuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
      </button>
    </nav>

    <!-- Mobile Menu -->
    <transition name="fade">
      <div
        v-if="menuOpen"
        class="md:hidden bg-background px-6 pb-6 pt-2 text-center text-white font-medium space-y-3"
      >
        <a href="#skills" class="block hover:text-primary" @click="closeMenu">Skills</a>
        <a href="#projects" class="block hover:text-primary" @click="closeMenu">Projects</a>
        <a href="#academics" class="block hover:text-primary" @click="closeMenu">Academics</a>
        <a href="#about" class="block hover:text-primary" @click="closeMenu">About</a>
        <a href="#contact" class="block hover:text-primary" @click="closeMenu">Contact</a>
      </div>
    </transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}

function closeMenu() {
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
