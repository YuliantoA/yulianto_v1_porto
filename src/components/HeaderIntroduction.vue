<template>
  <header
    class="flex flex-col justify-center my-auto items-start w-full h-[100vh] md:py-20 py-10 md:px-52 px-8 font-light"
  >
    <h1 class="text-2xl md:text-2xl lg:text-4xl xl:text-6xl">{{ title }}</h1>
    <h2
      class="text-2xl md:text-3xl lg:text-4xl xl:text-5xl text-left md:w-7/12 sm:w-6/12 w-full text md:leading-normal lg:leading-normal xl:leading-normal py-20"
      v-html="subtitle"
    ></h2>
    <div class="pb-10">
      <ButtonOutline
        @click="downloadCv"
        class="md:p-4 p-2 text-sm sm:text-base md:text-md lg:text-lg xl:text-xl"
        title="Download CV"
        :icon="['far', 'file-pdf']"
      />
    </div>
    <h3 class="text-xl md:text-2xl lg:text-3xl xl:text-4xl">
      Get in touch
      <span
        @click="openEmail"
        class="underline hover:bg-blue-theme transition-all ease-in duration-200 cursor-pointer hover:text-white"
        >{{ email }}</span
      >
    </h3>
  </header>
</template>

<script setup>
import ButtonOutline from "@/components/reusable/ButtonOutline.vue";
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
