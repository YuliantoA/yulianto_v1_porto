<script setup>
import HeaderIntroduction from "@/components/HeaderIntroduction.vue";
import BackgroundSummary from "@/components/BackgroundSummary.vue";
import SkillsProficient from "@/components/SkillsProficient.vue";
import WorkExperience from "@/components/WorkExperience.vue";
import ProjectHighlight from "@/components/ProjectHighlight.vue";
import FooterInformation from "@/components/FooterInformation.vue";
</script>

<template>
  <div>
    <HeaderIntroduction />
    <main>
      <BackgroundSummary />
      <SkillsProficient />
      <WorkExperience />
      <ProjectHighlight />
    </main>
    <FooterInformation />
  </div>
</template>

<style scoped></style>
