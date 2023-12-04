<template>
  <div
    class="w-full border border-black p-2 flex items-center justify-center gap-5 cursor-pointer rounded-md hover:bg-blue-theme hover:text-white text-black hover:animate-wiggle"
  >
    <font-awesome-icon v-if="icon" class="text-2xl" :icon="icon" />
    <span class="font-bold">{{ title }}</span>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  icon: {
    type: Array,
    required: false,
  },
});
</script>
