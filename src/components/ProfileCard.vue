<script setup>
import { ref, onMounted } from 'vue'

const typedText1 = ref('')
const typedText2 = ref('')
const showCursor = ref(true)

const part1 = "Hi!, "
const part2 = "I'm Melanie Abalde"

const typingSpeed = 100

onMounted(() => {
  let p1Index = 0
  let p2Index = 0

  function typePart1() {
    if (p1Index < part1.length) {
      typedText1.value += part1[p1Index]
      p1Index++
      setTimeout(typePart1, typingSpeed)
    } else {
      typePart2()
    }
  }

  function typePart2() {
    if (p2Index < part2.length) {
      typedText2.value += part2[p2Index]
      p2Index++
      setTimeout(typePart2, typingSpeed)
    }
  }

  // Start typing
  typePart1()
})
</script>

<template>
  <div class="w-full rounded-3xl bg-purple-50 p-8 shadow-sm relative">
    <!-- Window Controls -->
    <div class="mb-6 flex gap-2">
      <div class="h-3 w-3 rounded-full bg-pink-400"></div>
      <div class="h-3 w-3 rounded-full bg-purple-300"></div>
      <div class="h-3 w-3 rounded-full bg-yellow-200"></div>
    </div>

    <!-- Social Icons (Top Right Absolute) -->
    <div class="absolute top-8 right-8 flex gap-3">
      <!-- Github -->
      <a href="https://github.com/Araanna" target="_blank"
        class="text-purple-400 hover:text-purple-600 transition-colors" title="GitHub">
        <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="currentColor">
          <path
            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
        </svg>
      </a>
      <!-- LinkedIn -->
      <a href="https://www.linkedin.com/in/melanie-abalde-0a363a31b/" target="_blank"
        class="text-purple-400 hover:text-purple-600 transition-colors" title="LinkedIn">
        <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="currentColor">
          <path
            d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
        </svg>
      </a>
    </div>

    <div class="flex flex-col gap-8 md:flex-row md:items-center">
      <!-- Photo -->
      <div class="shrink-0">
        <div class="relative h-48 w-48 overflow-hidden rounded-2xl bg-yellow-200 shadow-inner">
          <!-- Placeholder for user image, using a cute gradient for now if no image -->
          <img src="../assets/images/mela.dev.jpg" alt="Profile"
            class="h-full w-full object-cover opacity-90 hover:scale-105 transition-transform duration-500" />
        </div>
      </div>

      <!-- Info -->
      <div class="flex-1 space-y-4">
        <!-- Greeting Headline -->
        <h1 class="text-4xl md:text-xl font-black text-slate-800 tracking-tight mb-2">
          <span>{{ typedText1 }}</span>
          <span class="text-purple-600">{{ typedText2 }}</span>
          <span class="animate-blink text-purple-600">|</span>
        </h1>

        <!-- Bio -->
        <p class="text-sm leading-relaxed text-slate-600">
          I’m a BS IT graduate majoring in Software Development and Applied Analytics in Business for IT based in
          Cagayan de Oro, with a strong interest in
          building large-scale, high-impact products. I focus on developing scalable systems while bringing a
          creative,
          design-driven perspective to technology.
        </p>

        <!-- Say Hi Button -->
        <div class="pt-4">
          <a href="mailto:mabalde2002@gmail.com"
            class="inline-flex items-center gap-2 px-2 py-1 rounded-lg border-2 border-purple-600 text-purple-600 font-bold hover:bg-purple-600 hover:text-white transition-all duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M20 4H4c-1.103 0-2 .897-2 2v12c0 1.103.897 2 2 2h16c1.103 0 2-.897 2-2V6c0-1.103-.897-2-2-2zm0 2v.511l-8 6.223-8-6.222V6h16zM4 18V9.044l7.386 5.745a.994.994 0 0 0 1.228 0L20 9.044 20.002 18H4z" />
            </svg>
            Say hi!
          </a>
        </div>

        <!-- Contact Grid Removed -->
      </div>
    </div>
  </div>
</template>

<style scoped>
.animate-blink {
  animation: blink 1s step-end infinite;
}

@keyframes blink {

  0%,
  100% {
    opacity: 1;
  }

  50% {
    opacity: 0;
  }
}
</style>
