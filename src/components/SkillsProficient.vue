<template>
  <CenterCard title="skills" class="text-left flex justify-between">
    <div v-for="{ section, values } in listSkill" :key="section">
      <div class="uppercase font-semibold mb-3">
        <span>{{ section }}</span>
      </div>
      <div v-for="value in values" :key="value" class="mb-2 font-light">
        {{ value }}
      </div>
    </div>
  </CenterCard>
</template>

<script setup>
import CenterCard from "@/components/reusable/CenterCard.vue";

const listSkill = [
  {
    section: "Languages",
    values: ["Javascript", "HTML", "CSS/Sass", "SQL", "VB.Net", "Python"],
  },
  {
    section: "Frameworks",
    values: ["Vue", "Tailwind CSS", "VITE"],
  },
  {
    section: "Tools",
    values: [
      "Bash",
      "Git & Github",
      "NPM",
      "Chrome DevTools",
      "Postman",
      "VS Code",
      "Visual Studio",
      "Internet Information Services",
    ],
  },
];
</script>
