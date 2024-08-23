<script setup lang="ts">
import { companys } from "@/constant";
</script>

<template>
  <section
    class="md:px-40 px-3 bg-dark flex flex-wrap max-md:gap-x-10 md:justify-between justify-evenly items-center border-t border-gray-600 z-50">
    <img
      v-for="(company, i) in companys"
      :key="i"
      :src="company.imgUrl"
      :alt="company.name"
      class="size-32 md:size-24" />
  </section>
</template>
