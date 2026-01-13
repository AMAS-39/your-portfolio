<script setup>
import { onMounted } from 'vue'   
import Navbar from './components/Navbar.vue'

import HeroSection from './components/HeroSection.vue'
import WhatIBuild from './components/WhatIBuild.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ResearchPublications from './components/ResearchPublications.vue'
import ExperienceSection from './components/Experience.vue'
import LeadershipTeaching from './components/LeadershipTeaching.vue'
import AcademicsSection from './components/AcademicsSection.vue'
import AboutMe from './components/AboutMe.vue'
import ContactMe from './components/ContactMe.vue'

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
  <WhatIBuild />
  <SkillsSection />
  <ProjectsSection />
  <ResearchPublications />
  <ExperienceSection />
  <LeadershipTeaching />
  <AcademicsSection />
  <AboutMe />
  <ContactMe />

</template>