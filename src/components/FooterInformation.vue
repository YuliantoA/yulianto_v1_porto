<template>
  <footer class="h-[10vh] pb-16">
    <section
      class="flex md:flex-row flex-col justify-between items-center h-full w-full md:px-52 px-8"
    >
      <div class="w-full text-center md:text-left md:w-3/12">
        <p class="xl:text-xl lg:text-lg md:text-md text-sm font-semibold">
          Design inspired by Brittany Chiang, Developed by Yulianto
        </p>
      </div>
      <div
        class="w-2/12 flex justify-around items-center text-xl font-semibold text-blue-theme"
        :class="[isMobile(width) ? ' pb-5 gap-5' : '']"
      >
        <div
          v-for="({ title, link, icon }, index) in listContact"
          :key="index"
          @click="openLink(link)"
          class="cursor-pointer hover:animate-wiggle hover:underline hover:underline-offset-4 uppercase"
        >
          <font-awesome-icon
            v-if="isMobile(width)"
            class="text-2xl mt-5"
            :icon="icon"
          />
          <span v-else>
            {{ title }}
          </span>
        </div>
      </div>
    </section>
  </footer>
</template>

<script setup>
const email = import.meta.env.VITE_APP_EMAIL;
const gitUrl = import.meta.env.VITE_APP_GITURL;
import { isMobile } from "@/util/helper.js";
import { useWindowSize } from "@vueuse/core";
const { width } = useWindowSize();
const listContact = [
  {
    title: "email",
    link: "mailto:" + email,
    icon: ["far", "envelope"],
  },
  {
    title: "github",
    link: gitUrl,
    icon: ["fab", "github"],
  },
];
function openLink(url) {
  window.open(url, "_blank", "noreferrer");
}
</script>
