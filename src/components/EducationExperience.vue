<template>
  <CenterCard title="Education" class="text-left flex flex-col">
    <div
      v-for="({ university, role, tanggal }, index) in listExperience"
      :key="index"
      class="flex justify-between mb-5"
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
      <div class="font-light">
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
