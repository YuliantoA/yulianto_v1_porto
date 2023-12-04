<template>
  <CenterCard title="Experience">
    <div
      v-for="({ company, role, tanggal }, index) in listExperience"
      :key="index"
      class="w-full flex lg:flex-row flex-col justify-between mb-5 xl:text-xl lg:text-lg md:text-md text-base md:gap-5 gap-0"
    >
      <div>
        <div class="font-semibold capitalize">
          <span>
            {{ company }}
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
    company: "Bank Indonesia",
    role: "Software Engineer",
    tanggal: "2021 - Juli 2023 (2,5 years)",
  },
  {
    company: "Evermos",
    role: "Intern Quality Assurance",
    tanggal: "2019 - 2020 (~1 years)",
  },
];
</script>
