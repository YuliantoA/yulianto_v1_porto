<script setup>
import HeaderIntroduction from "@/components/HeaderIntroduction.vue";
import BackgroundSummary from "@/components/BackgroundSummary.vue";
import SkillsProficient from "@/components/SkillsProficient.vue";
import WorkExperience from "@/components/WorkExperience.vue";
import ProjectHighlight from "@/components/ProjectHighlight.vue";
import FooterInformation from "@/components/FooterInformation.vue";
import EducationExperience from "@/components/EducationExperience.vue";

import { vScrollReveal } from "vue-scroll-reveal";
</script>

<template>
  <div>
    <HeaderIntroduction v-scroll-reveal="{ delay: 100 }" />
    <main>
      <BackgroundSummary v-scroll-reveal="{ delay: 100 }" />
      <EducationExperience v-scroll-reveal="{ delay: 100 }" />
      <SkillsProficient v-scroll-reveal="{ delay: 100 }" />
      <WorkExperience v-scroll-reveal="{ delay: 100 }" />
      <ProjectHighlight v-scroll-reveal="{ delay: 100 }" />
    </main>
    <FooterInformation v-scroll-reveal />
  </div>
</template>

<style scoped></style>
