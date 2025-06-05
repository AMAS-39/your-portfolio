<template>
  <section id="experience" class="bg-background text-white py-20 px-6">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-4xl sm:text-5xl font-bold text-primary mb-16 text-center">Experience</h2>

      <div class="relative border-l border-primary pl-6 space-y-14">
        <div
          v-for="(job, index) in experiences"
          :key="index"
          class="relative group"
          data-aos="fade-up"
        >
          <div class="absolute w-4 h-4 bg-primary rounded-full -left-2.5 top-2"></div>

          <div class="bg-gray-800 p-6 rounded-xl shadow-lg hover:shadow-2xl transition duration-300">
            <div class="flex flex-col sm:flex-row sm:justify-between sm:items-center">
              <h3 class="text-2xl font-semibold text-primary mb-2 sm:mb-0">{{ job.role }}</h3>
              <span class="text-sm text-gray-400 italic">{{ job.duration }}</span>
            </div>
            <p class="text-gray-400 mt-1">{{ job.company }}</p>

            <ul class="list-disc list-inside text-gray-300 mt-4 space-y-1">
              <li v-for="(duty, i) in job.details" :key="i">{{ duty }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const experiences = [
  {
    role: 'Head of Technology & Innovation',
    company: 'Korea Kurdistan Youth Organization (KKYO)',
    duration: 'Dec 2024 – Present',
    details: [
      'Leading the Technology & Innovation Department',
      'Developed the KKYO Website & Admin Panel (Vue.js & Flask)',
      'Managing tech-driven initiatives to enhance digital transformation'
    ]
  },
  {
    role: 'Front-End Developer',
    company: 'Soft 4 U Company, Erbil, Iraq',
    duration: 'Jan 2025 – Present',
    details: [
      'Developing and maintaining front-end components of web applications',
      'Collaborating with design/backend teams to improve UI/UX',
      'Ensuring the technical feasibility of UI designs'
    ]
  },
  {
    role: 'Student Representative',
    company: 'Computer Education Department, TIU',
    duration: 'Oct 2024 – Present',
    details: [
      'Representing students in academic and administrative discussions',
      'Organizing meetings, workshops, and addressing student concerns'
    ]
  },
  {
    role: 'Assistant Lecturer Intern',
    company: 'Optimal Source Development – Code Lab, Erbil',
    duration: 'Oct 2024 – Dec 2024',
    details: [
      'Assisted in teaching Scratch to children and teenagers',
      'Supported classroom activities and answered queries'
    ]
  },
  {
    role: 'Front-End Developer Intern',
    company: 'Pirmam Company, Erbil, Iraq',
    duration: 'Aug 2024 – Oct 2024',
    details: [
      'Assisted in UI development for client projects',
      'Gained practical experience in modern web technologies'
    ]
  }
];
</script>

<style scoped>
/* Optional: Animate the dot on hover */
.group:hover .dot {
  transform: scale(1.2);
}
</style>
