<template>
  <footer class="h-[10vh]">
    <section class="flex justify-between items-center h-full w-full px-20">
      <div class="w-2/12">
        <p class="text-xl font-semibold">
          Design inspired by Brittany Chiang, Developed by Yulianto
        </p>
      </div>
      <div
        class="w-2/12 flex justify-around items-center text-xl font-semibold text-blue-theme"
      >
        <div
          v-for="({ title, link }, index) in listContact"
          :key="index"
          @click="openLink(link)"
          class="cursor-pointer hover:animate-wiggle hover:underline hover:underline-offset-4 uppercase"
        >
          {{ title }}
        </div>
      </div>
    </section>
  </footer>
</template>

<script setup>
const email = import.meta.env.VITE_APP_EMAIL;
const gitUrl = import.meta.env.VITE_APP_GITURL;
const listContact = [
  {
    title: "email",
    link: "mailto:" + email,
  },
  {
    title: "github",
    link: gitUrl,
  },
];
function openLink(url) {
  window.open(url, "_blank", "noreferrer");
}
</script>
