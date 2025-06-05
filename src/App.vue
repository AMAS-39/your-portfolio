<script setup>
import { onMounted } from 'vue'   
import Navbar from './components/Navbar.vue'

import HeroSection from './components/HeroSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import AcademicsSection from './components/AcademicsSection.vue'
import AboutMe from './components/AboutMe.vue'
import ContactMe from './components/ContactMe.vue'
import ExperienceSection from './components/Experience.vue'

import AOS from 'aos'
import 'aos/dist/aos.css'

onMounted(() => {
  AOS.init({
    once: true,
    duration: 800,
  })
})
</script>


<template>
  <Navbar />
  <HeroSection />
  <SkillsSection />
  <ProjectsSection />
  <ExperienceSection />
  <AcademicsSection />
  <AboutMe />
  <ContactMe />

</template>