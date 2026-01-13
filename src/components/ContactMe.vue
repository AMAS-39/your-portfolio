<template>
  <section id="contact" class="bg-background text-white py-20 px-6">
    <div class="max-w-4xl mx-auto">
      <h2 class="text-4xl sm:text-5xl font-bold text-primary mb-10 text-center">Get In Touch</h2>
      <p class="text-gray-300 text-md mb-12 text-center">
        Feel free to reach out for collaborations, freelance work, or just a tech chat.
      </p>

      <div class="flex flex-wrap justify-center gap-6 mb-16">
        <!-- WhatsApp -->
        <a
          href="https://wa.me/9647507180285"
          target="_blank"
          class="bg-green-500 hover:bg-green-600 text-white px-5 py-3 rounded-lg flex items-center gap-2 transition"
        >
          <i class="fab fa-whatsapp"></i> WhatsApp
        </a>

        <!-- Email -->
        <a
          href="mailto:ahmadshwanaswad@gmail.com"
          class="bg-blue-600 hover:bg-blue-700 text-white px-5 py-3 rounded-lg flex items-center gap-2 transition"
        >
          <i class="fas fa-envelope"></i> Email
        </a>

        <!-- GitHub -->
        <a
          href="https://github.com/AMAS-39"
          target="_blank"
          class="bg-gray-800 hover:bg-gray-900 text-white px-5 py-3 rounded-lg flex items-center gap-2 transition"
        >
          <i class="fab fa-github"></i> GitHub
        </a>

        <!-- LinkedIn -->
        <a
          href="https://www.linkedin.com/in/ahmad-shwan-b304b527b/"
          target="_blank"
          class="bg-blue-800 hover:bg-blue-900 text-white px-5 py-3 rounded-lg flex items-center gap-2 transition"
        >
          <i class="fab fa-linkedin"></i> LinkedIn
        </a>
      </div>

      <!-- Footer Information -->
      <footer class="border-t border-gray-700 pt-8 mt-12">
        <div class="flex flex-col sm:flex-row justify-between items-center gap-4 text-gray-400 text-sm">
          <div class="flex flex-wrap justify-center gap-4">
            <a href="https://github.com/AMAS-39" target="_blank" class="hover:text-primary transition">
              <i class="fab fa-github"></i> github.com/AMAS-39
            </a>
            <a href="mailto:ahmadshwanaswad@gmail.com" class="hover:text-primary transition">
              <i class="fas fa-envelope"></i> ahmadshwanaswad@gmail.com
            </a>
          </div>
          <div class="flex flex-wrap justify-center gap-4">
            <span><i class="fas fa-map-marker-alt"></i> Erbil, Kurdistan, Iraq</span>
            <a href="https://ahmadcode.tech" target="_blank" class="hover:text-primary transition">
              <i class="fas fa-globe"></i> ahmadcode.tech
            </a>
          </div>
        </div>
        <div class="text-center text-gray-500 text-xs mt-6">
          <p>&copy; {{ new Date().getFullYear() }} Ahmad Shwan. All rights reserved.</p>
        </div>
      </footer>
    </div>
  </section>
</template>




