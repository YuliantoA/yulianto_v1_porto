<template>
  <section
    class="w-full h-full flex items-center justify-center xl:px-40 lg:px-32 px-8 py-24"
  >
    <div
      id="card"
      class="md:w-11/12 w-full flex flex-col items-start justify-around gap-10"
      :class="[cardBreakpoint + ':flex-row']"
    >
      <div
        class="w-1/12 md:w-4/12 lg:w-3/12 text-right tracking-widest text-blue-theme font-bold uppercase mr-auto lg:text-xl md:text-lg text-md"
      >
        <span>{{ title }}</span>
      </div>
      <div
        class="w-11/12 lg:w-9/12"
        :class="[cardBreakpoint === 'md' ? 'md:w-8/12' : '']"
        :="$attrs"
      >
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
  cardBreakpoint: {
    type: String,
    required: false,
    default: "md",
  },
});
</script>
