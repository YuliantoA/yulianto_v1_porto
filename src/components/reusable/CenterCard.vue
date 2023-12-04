<template>
  <section class="w-full h-full flex items-center justify-center p-40">
    <div id="card" class="w-9/12 flex items-start justify-center text-xl">
      <div
        class="w-3/12 text-right tracking-widest text-blue-theme font-bold uppercase mr-auto"
      >
        <span>{{ title }}</span>
      </div>
      <div class="w-7/12" :="$attrs">
        <slot></slot>
      </div>
      <div class="w-1/12"></div>
    </div>
  </section>
</template>

<script setup>
defineOptions({
  inheritAttrs: false,
});
defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>
