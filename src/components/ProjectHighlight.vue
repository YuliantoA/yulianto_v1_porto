<template>
  <CenterCard
    title="Featured Project"
    class="text-left flex flex-col justify-between gap-20"
  >
    <div
      class="w-full flex justify-between gap-10"
      v-for="(
        { title, description, img, linkGit, linkDemo }, index
      ) in listProject"
      :key="index"
    >
      <div class="w-9/12">
        <img class="w-full" :src="img" />
      </div>
      <div class="w-3/12 flex flex-col justify-start items-start gap-5">
        <div class="font-bold capitalize">
          <span>
            {{ title }}
          </span>
        </div>
        <p class="font-light text-base">{{ description }}</p>
        <ButtonOutline
          title="Github"
          :icon="['fab', 'github']"
          @click="openLink(linkGit)"
        />
        <ButtonOutline title="Demo" @click="openLink(linkDemo)" />
      </div>
    </div>
  </CenterCard>
</template>

<script setup>
import ButtonOutline from "@/components/reusable/ButtonOutline.vue";
import CenterCard from "@/components/reusable/CenterCard.vue";

const listProject = [
  {
    title: "KajianKuy",
    description:
      "Responsive web Project to share kajian from all muslim, design inspired from linkedin, use Vue 3 with Tailwind CSS as front end and firebase as realtime database, storage and authentication service",
    img: new URL("/src/assets/images/kajiankuy.png", import.meta.url),
    linkGit: "https://github.com/YuliantoA/porto",
    linkDemo: "https://kajiankuy.netlify.app/",
  },
  {
    title: "Quiz Lieur",
    description:
      "Responsive quiz web app that consume Rest API from opentdb.com, create using Vue 3 with Tailwind CSS and some Vue Ecosystem (Pinia, Vue-Router, Axios)",
    img: new URL("/src/assets/images/quizlieur.png", import.meta.url),
    linkGit: "https://github.com/YuliantoA/quiz",
    linkDemo: "https://quizlieur.netlify.app/",
  },
];

function openLink(url) {
  window.open(url, "_blank", "noreferrer");
}
</script>
