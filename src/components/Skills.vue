<template>
  <FolderCard title="Skills">
    <div class="grid grid-cols-2 gap-4 text-sm text-slate-700">
      <div>
        <h4 class="font-bold mb-2 text-purple-600">Frontend</h4>
        <ul class="list-disc ml-4 space-y-1">
          <li>Vue.js</li>
          <li>Tailwind CSS</li>
          <li>JavaScript (ES6+)</li>
          <li>HTML5 & CSS3</li>
        </ul>
        <h4 class="font-bold mb-2 text-purple-600 mt-4">Backend</h4>
        <ul class="list-disc ml-4 space-y-1">
          <li>PostgreSQL</li>
          <li>Docker</li>
        </ul>
      </div>
      <div>
        <h4 class="font-bold mb-2 text-purple-600">Tools & Design</h4>
        <ul class="list-disc ml-4 space-y-1">
          <li>Git & GitHub</li>
          <li>Figma</li>
          <li>VS Code</li>
          <li>Adobe Creative Suite</li>
        </ul>
      </div>
    </div>
  </FolderCard>
</template>

<script setup>
import FolderCard from './FolderCard.vue'
</script>
