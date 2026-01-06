<template>
  <div class="min-h-screen bg-slate-50 flex flex-col relative">
    <LiquidEther :colors="['#5227FF', '#FF9FFC', '#B19EEF']" :mouseForce="20" :cursorSize="100" :isViscous="true"
      :viscous="30" :iterationsViscous="32" :iterationsPoisson="32" :resolution="0.5" :isBounce="true" :autoDemo="true"
      :autoSpeed="0.5" :autoIntensity="2.2" :takeoverDuration="0.25" :autoResumeDelay="3000" :autoRampDuration="0.6"
      class="fixed top-0 left-0 z-0" />
    <div class="relative z-10 flex-1 w-full max-w-5xl mx-auto py-10 px-4 md:px-8 space-y-12">

      <!-- Top Profile Section -->
      <ProfileCard />

      <!-- Main Content Grid -->
      <div class="grid grid-cols-1 gap-6 md:grid-cols-2 items-start">

        <!-- Left Column -->
        <div class="space-y-6">
          <!-- About Me -->
          <AboutMe />

          <!-- Work Experience -->
          <!-- Work Experience -->
          <WorkExperience />

          <!-- Community & Leadership -->
          <FolderCard title="Community & Leadership">
            <!-- Item 1 -->
            <div class="mb-5">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold text-slate-800 text-sm">Volunteer Coach</h3>
                <span class="rounded-lg bg-pink-100 px-2 py-0.5 text-[10px] font-bold text-pink-600">July 2025</span>
              </div>
              <p class="text-xs text-slate-500 italic mb-1">Django Girls CDO</p>
              <p class="text-xs text-slate-600">Guided first-time developers in building Python/Django apps.</p>
            </div>

            <!-- Item 2 -->
            <div class="mb-5">
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold text-slate-800 text-sm">Fullstack Bootcamp</h3>
                <span class="rounded-lg bg-blue-100 px-2 py-0.5 text-[10px] font-bold text-blue-600">May 2024</span>
              </div>
              <p class="text-xs text-slate-500 italic mb-1">Fligno</p>
              <p class="text-xs text-slate-600">Backend with Laravel, Frontend with React/Redux.</p>
            </div>

            <!-- Item 3 -->
            <div>
              <div class="flex justify-between items-center mb-1">
                <h3 class="font-bold text-slate-800 text-sm">SBO Associate Treasurer</h3>
                <span class="rounded-lg bg-green-100 px-2 py-0.5 text-[10px] font-bold text-green-600">July 2021</span>
              </div>
              <p class="text-xs text-slate-500 italic mb-1">Student Body Organization</p>
              <p class="text-xs text-slate-600">Financial management and event planning.</p>
            </div>
          </FolderCard>
        </div>

        <!-- Right Column -->
        <div class="space-y-6">
          <!-- Education -->
          <FolderCard title="Education">
            <div class="mb-4">
              <div class="flex justify-between items-start mb-1">
                <h3 class="text-sm font-bold text-slate-800">BS in Information Technology</h3>
                <span
                  class="rounded-full bg-purple-100 px-3 py-1 text-[10px] font-bold text-purple-600 whitespace-nowrap ml-2">Dean's
                  Lister</span>
              </div>
              <p class="text-xs text-slate-500 italic mb-2">PHINMA – Cagayan de Oro College</p>
              <ul class="space-y-2 text-xs text-slate-600">
                <li class="flex items-start gap-2"><span class="text-purple-400 mt-[2px]">✦</span><span>Major in System
                    Development</span></li>
                <li class="flex items-start gap-2"><span class="text-purple-400 mt-[2px]">✦</span><span>Dean's Lister
                    1st & 2nd Semester, 2021</span></li>
              </ul>
            </div>
          </FolderCard>

          <!-- Certifications & Training -->
          <!-- Certifications & Training -->
          <Certifications />

          <!-- Skills -->
          <FolderCard title="Core Skills">
            <div class="flex flex-wrap gap-2">
              <span class="px-3 py-1 bg-slate-100 text-slate-600 rounded-full text-xs font-semibold">Python
                (Django)</span>
              <span class="px-3 py-1 bg-blue-100 text-blue-600 rounded-full text-xs font-semibold">React.js</span>
              <span class="px-3 py-1 bg-green-100 text-green-600 rounded-full text-xs font-semibold">Vue.js</span>
              <span class="px-3 py-1 bg-black text-white rounded-full text-xs font-semibold">Next.js</span>
              <span class="px-3 py-1 bg-cyan-100 text-cyan-600 rounded-full text-xs font-semibold">Tailwind CSS</span>
              <span class="px-3 py-1 bg-purple-100 text-purple-600 rounded-full text-xs font-semibold">Bootstrap</span>
              <span class="px-3 py-1 bg-orange-100 text-orange-600 rounded-full text-xs font-semibold">HTML5/CSS3</span>
              <span class="px-3 py-1 bg-yellow-100 text-yellow-600 rounded-full text-xs font-semibold">MySQL</span>
              <span class="px-3 py-1 bg-red-100 text-red-600 rounded-full text-xs font-semibold">RESTful APIs</span>
              <span class="px-3 py-1 bg-slate-200 text-slate-700 rounded-full text-xs font-semibold">Git</span>
              <span class="px-3 py-1 bg-orange-50 text-orange-500 rounded-full text-xs font-semibold">Postman</span>
              <span class="px-3 py-1 bg-blue-50 text-blue-500 rounded-full text-xs font-semibold">Flutter</span>
              <span class="px-3 py-1 bg-indigo-50 text-indigo-500 rounded-full text-xs font-semibold">Figma</span>
            </div>
          </FolderCard>
        </div>
      </div>

      <!-- School & Personal Projects Section -->
      <div class="space-y-6">
        <h2 class="text-2xl font-bold text-slate-800">School & Personal Projects</h2>

        <!-- Featured Project Spotlight -->
        <ProjectSpotlight />
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6">

          <!-- Project 1: Siargao Travel Website -->
          <div
            class="group flex flex-col justify-between rounded-xl bg-purple-50 p-6 transition-all hover:-translate-y-1 hover:shadow-md">
            <div>
              <div class="mb-4 flex items-center justify-between text-purple-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="1.5">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
                </svg>
                <div class="flex gap-3">
                  <a href="https://github.com/Araanna/Siargao-Travel-and-Tour-Website" target="_blank"
                    class="hover:text-purple-800">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                    </svg>
                  </a>
                </div>
              </div>
              <h3 class="mb-2 text-lg font-bold text-slate-800 group-hover:text-purple-600 transition-colors">Siargao
                Travel Website</h3>
              <p class="mb-4 text-sm leading-relaxed text-slate-600">
                Responsive travel booking website allowing users to browse destinations and book tours securely.
              </p>
            </div>
            <div class="flex flex-wrap gap-2 text-xs font-medium text-slate-500">
              <span>VueJS</span>
              <span>PHP</span>
              <span>MySQL</span>
            </div>
          </div>

          <!-- Project 2: Student Expense Tracker -->
          <div
            class="group flex flex-col justify-between rounded-xl bg-purple-50 p-6 transition-all hover:-translate-y-1 hover:shadow-md">
            <div>
              <div class="mb-4 flex items-center justify-between text-purple-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="1.5">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
                </svg>
                <div class="flex gap-3">
                  <a href="https://github.com/Araanna/FASTAPI-PHINMA-COC-STUDENT-EXPENSE-TRACKER" target="_blank"
                    class="hover:text-purple-800">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                    </svg>
                  </a>
                </div>
              </div>
              <h3 class="mb-2 text-lg font-bold text-slate-800 group-hover:text-purple-600 transition-colors">Student
                Expense Tracker</h3>
              <p class="mb-4 text-sm leading-relaxed text-slate-600">
                Mobile budgeting app enabling students to track expenses and set budgets with transaction APIs.
              </p>
            </div>
            <div class="flex flex-wrap gap-2 text-xs font-medium text-slate-500">
              <span>Flutter</span>
              <span>FastAPI</span>
            </div>
          </div>



          <!-- Project 4: Unity RPG Game -->
          <div
            class="group flex flex-col justify-between rounded-xl bg-purple-50 p-6 transition-all hover:-translate-y-1 hover:shadow-md">
            <div>
              <div class="mb-4 flex items-center justify-between text-purple-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="1.5">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
                </svg>
                <div class="flex gap-3">
                  <a href="https://github.com/Araanna/gamedev_website" target="_blank" class="hover:text-purple-800">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                    </svg>
                  </a>
                </div>
              </div>
              <h3 class="mb-2 text-lg font-bold text-slate-800 group-hover:text-purple-600 transition-colors">Unity RPG
                Game</h3>
              <p class="mb-4 text-sm leading-relaxed text-slate-600">
                2D platformer RPG built in Unity, implementing animation, collision detection, and player movement.
              </p>
            </div>
            <div class="flex flex-wrap gap-2 text-xs font-medium text-slate-500">
              <span>Unity</span>
              <span>C#</span>
            </div>
          </div>

          <!-- Project 3: Reservation Monitoring System (Moved) -->
          <div
            class="group flex flex-col justify-between rounded-xl bg-purple-50 overflow-hidden transition-all hover:-translate-y-1 hover:shadow-md">

            <!-- Top Section: Icons (Lighter) -->
            <div class="p-6 pb-0">
              <div class="mb-4 flex items-center justify-between text-purple-600">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="1.5">
                  <path stroke-linecap="round" stroke-linejoin="round"
                    d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z" />
                </svg>
                <div class="flex gap-3">
                  <a href="https://github.com/Araanna/IT-DAYS-WEB-APP" target="_blank" class="hover:text-purple-800">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                    </svg>
                  </a>
                </div>
              </div>
            </div>

            <!-- Bottom Section: Info (Darker) -->
            <div class="bg-purple-100/60 p-6 pt-4 mt-auto">
              <h3 class="mb-2 text-lg font-bold text-slate-800 group-hover:text-purple-600 transition-colors">
                Reservation Monitoring System</h3>
              <p class="mb-4 text-sm leading-relaxed text-slate-600">
                Capstone project implementing a full-scale reservation and monitoring system for campus facilities,
                significantly improving administrative efficiency.
              </p>
              <div class="flex flex-wrap gap-2 text-xs font-medium text-slate-500">
                <span>Flutter</span>
                <span>ReactJS</span>
                <span>PHP</span>
              </div>
            </div>
          </div>

        </div>
      </div>

      <Highlights />
    </div>

    <div ref="footerRef" class="relative z-[60] bg-slate-50">
      <Footer />
    </div>

    <!-- Global Bottom Gradual Blur -->
    <GradualBlur target="page" position="bottom" height="6rem" :strength="2" :divCount="5" :zIndex="50"
      class="fixed bottom-0 left-0 w-full pointer-events-none transition-opacity duration-300"
      :style="{ opacity: isFooterVisible ? 0 : 1 }" />
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import ProfileCard from './components/ProfileCard.vue'
import Certifications from './components/Certifications.vue'
import WorkExperience from './components/WorkExperience.vue'

import FolderCard from './components/FolderCard.vue'
import Highlights from './components/Highlights.vue'
import Footer from './components/Footer.vue'
import ProjectSpotlight from './components/ProjectSpotlight.vue'
import GradualBlur from './components/GradualBlur.vue'
import LiquidEther from './components/LiquidEther.vue'

const footerRef = ref(null)
const isFooterVisible = ref(false)
let observer = null

onMounted(() => {
  observer = new IntersectionObserver(([entry]) => {
    isFooterVisible.value = entry.isIntersecting
  }, { threshold: 0, rootMargin: '100px' })
  if (footerRef.value) {
    observer.observe(footerRef.value)
  }
})

onUnmounted(() => {
  if (observer) observer.disconnect()
})
</script>
