<template>
  <header
    class="flex flex-col justify-around my-auto items-start w-full h-[100vh] p-52 font-light"
  >
    <h1 class="text-6xl">{{ title }}</h1>
    <h2
      class="text-5xl text-left w-7/12 text leading-relaxed"
      v-html="subtitle"
    ></h2>
    <div class="w-2/12">
      <ButtonOutline
        @click="downloadCv"
        class="p-4 text-2xl"
        title="Download CV"
        :icon="['far', 'file-pdf']"
      />
    </div>
    <h3 class="text-3xl">
      Get in touch
      <span
        @click="openEmail"
        class="underline hover:bg-blue-400 transition-all ease-in duration-200 cursor-pointer hover:text-white"
        >{{ email }}</span
      >
    </h3>
  </header>
</template>

<script setup>
import ButtonOutline from "./reusable/ButtonOutline.vue";
const title = "Hello! 👋";
const subtitle =
  "I am <b>Yulianto Ardi N</b>, an aspiring front-end software engineer with a keen interest in crafting visually appealing interfaces and creating engaging user experiences. 💕";

const email = import.meta.env.VITE_APP_EMAIL;
const cv = import.meta.env.VITE_APP_CV;
function downloadCv() {
  let link = document.createElement("a");
  link.href = "/files/" + cv;
  link._target = "blank";
  link.click();
}

function openEmail() {
  window.open("mailto:" + email, "_blank", "noreferrer");
}
</script>
