<template>
  <CenterCard
    title="skills"
    class="text-left flex md:justify-between justify-around lg:text-xl md:text-lg text-md gap-5 md:flex-nowrap flex-wrap"
  >
    <template v-for="({ section, values }, index) in listSkill" :key="index">
      <div
        v-if="index % 2 === 0 && isMobile(width)"
        class="h-0 basis-full"
      ></div>
      <div :class="[index === listSkill.length - 1 ? 'self-start' : '']">
        <div class="uppercase font-semibold mb-3">
          <span>{{ section }}</span>
        </div>
        <div v-for="value in values" :key="value" class="mb-2 font-light">
          {{ value }}
        </div>
      </div>
    </template>
  </CenterCard>
</template>

<script setup>
import CenterCard from "@/components/reusable/CenterCard.vue";
import { isMobile } from "@/util/helper.js";
import { useWindowSize } from "@vueuse/core";
const { width } = useWindowSize();

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
