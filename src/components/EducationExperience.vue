<template>
  <CenterCard title="Education">
    <div
      v-for="({ university, role, tanggal }, index) in listExperience"
      :key="index"
      class="w-full flex lg:flex-row flex-col justify-between mb-5 lg:text-md text-base"
    >
      <div>
        <div class="font-semibold capitalize">
          <span>
            {{ university }}
          </span>
        </div>
        <div class="font-light capitalize">
          <span>
            {{ role }}
          </span>
        </div>
      </div>
      <div class="font-light lg:text-md md:text-base text-sm">
        <span>
          {{ tanggal }}
        </span>
      </div>
    </div>
  </CenterCard>
</template>

<script setup>
import CenterCard from "@/components/reusable/CenterCard.vue";

const listExperience = [
  {
    university: "Institut Teknologi Nasional Bandung",
    role: "Informatic Engineering (Best Graduate)",
    tanggal: "2016 - 24 Oktober 2020",
  },
];
</script>
