<template>
    <main class="flex flex-col flex-auto lg:flex-row overflow-hidden bg-gray-900 text-white">
      <div id="mobile-page-title" class="text-center py-4">
        <h2 class="text-2xl font-bold">_experience</h2>
      </div>
  
      <div class="flex flex-col w-full overflow-hidden p-5">
        <div id="experience-case" class="grid grid-cols-1 gap-4 lg:grid-cols-2 max-w-full h-full overflow-scroll lg:self-center">
          <div v-for="item in experienceItems" :key="item.title" class="experience-card p-5 rounded-lg bg-gray-800 shadow-lg transform transition-transform ">
            <div class="flex items-center mb-3">
            
              <h4 class="text-md font-semibold">{{ item.title }}</h4>
            </div>
            <p class="text-gray-400">{{ item.description }}</p>
          </div>
        </div>
        <div class="flex justify-center mt-5">
            <a href="https://www.linkedin.com/in/rafaelnuansa/details/experience/" target="_blank" class="px-4 py-2 bg-blue-600 rounded-lg hover:bg-blue-700 transition-colors">More Detail Experience on LinkedIn</a>
        </div>
      </div>
    </main>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const experienceItems = ref([
    {
      title: "Freelance Web Developer at POSX Solutions (Brunei Darussalam) Des 2023 - May 2024",
      description: "Worked on various web development projects...",
    },
    {
      title: "Senior Web Developer at Universitas Djuanda (Jul 2021 - Saat ini)",
      description: "Leading the development team and managing...",
    },
    {
      title: "Middle Web Developer at Universitas Djuanda (Mei 2020 - Jul 2021)",
      description: "Focused on backend development...",
    },
    {
      title: "Junior Web Developer at Universitas Djuanda (Jan 2019 - Jul 2020)",
      description: "Assisted in various web development tasks...",
    },
    {
      title: "Freelance Web Developer (Jan 2018 - Saat ini)",
      description: "Working with multiple clients on freelance projects...",
    },
    {
      title: "Web Developer at Bina Iman Mulia (Nov 2023 - Jan 2024 · 3 bln)",
      description: "Developed and maintained web applications...",
    },
    {
      title: "Freelance Backend Developer at Refourma.com - Semarang Jawa Tengah (Feb 2023 - Mar 2023 · 2 bln)",
      description: "Focused on backend systems and API development...",
    }
  ])
  </script>
  
  <style>
  #experience-case {
    padding: 25px 25px 5px;
  }
  
  .experience-card {
    background-color: #1C2B3A;
  }
  
  @media (max-width: 768px) {
    #experience-case {
      padding: 0px 25px 40px;
    }
  }
  
  @media (min-width: 768px) {
    #experience-case {
      padding: 50px 50px 40px;
    }
  }
  
  @media (min-width: 1350px) {
    #experience-case {
      padding: 50px 80px 40px;
    }
  }
  </style>
  