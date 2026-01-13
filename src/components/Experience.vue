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
    role: 'Full-Stack Software Developer (Part-Time)',
    company: 'Cars Colosseum Company – Erbil, Iraq',
    duration: 'Nov 2025 – Present',
    details: [
      'Developing and maintaining a cross-platform mobile application using React Native with a Laravel backend.',
      'Designing RESTful APIs, handling database logic, authentication, and core system features.',
      'Integrating mobile and backend systems to ensure secure, scalable, and efficient data flow.'
    ]
  },
  {
    role: 'Mobile Application Developer (Part-Time)',
    company: 'TechEye Company – Erbil, Iraq',
    duration: 'Jul 2025 – Present',
    details: [
      'Building and maintaining Flutter applications integrated with Firebase services.',
      'Collaborating with backend and design teams to deliver high-performance mobile solutions.',
      'Implementing real-time features and AI-driven functionality.'
    ]
  },
  {
    role: 'Front-End & AI Developer',
    company: 'Soft 4 You Agency – Erbil, Iraq (Remote)',
    duration: 'Jan 2025 – Present',
    details: [
      'Developing AI-enhanced UI/UX components and intelligent web interfaces.',
      'Integrating Vue.js front-ends with Flask backends for smart, data-driven applications.'
    ]
  },
  {
    role: 'Computer Science Teacher Intern',
    company: 'Cambridge International Kurdistan School – Erbil, Iraq',
    duration: 'Oct 2025 – Present',
    details: [
      'Teaching programming fundamentals and computational thinking to high-school students.',
      'Designing simplified learning materials for Python and C++, and supervising small coding projects.'
    ]
  },
  {
    role: 'Head of Technology & Innovation Department',
    company: 'Korea Kurdistan Youth Organization (KKYO)',
    duration: 'Dec 2024 – Present',
    details: [
      'Leading technology initiatives and managing the Technology & Innovation Department.',
      'Designed and developed the KKYO website and admin system using Vue.js and Flask.'
    ]
  },
  {
    role: 'Front-End Developer Intern',
    company: 'Soft 4 You Agency – Erbil, Iraq (Remote)',
    duration: 'Jun 2024 – Dec 2024',
    details: [
      'Assisted in front-end development using Vue.js and Tailwind CSS.',
      'Collaborated with designers and backend developers on responsive UI and API integration.'
    ]
  },
  {
    role: 'Front-End Developer Intern',
    company: 'Pirmam Company – Erbil, Iraq',
    duration: 'Aug 2024 – Oct 2024',
    details: [
      'Assisting in developing user interfaces for client projects.',
      'Gaining practical experience in modern web development technologies.'
    ]
  },
  {
    role: 'Assistant Lecturer Intern',
    company: 'Optimal Source Development – Code Lab – Erbil, Iraq',
    duration: 'Oct 2024 – Dec 2024',
    details: [
      'Assisting in teaching Scratch programming to children and teenagers.',
      'Supporting hands-on classroom activities and student exercises.'
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
