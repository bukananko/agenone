<script setup lang="ts">
import { benefits } from '@/constant';
</script>

<template>
  <div class="relative hidden md:flex justify-center items-center">
    <div class="absolute -top-14 bg-primary px-20 py-3 rounded-t-2xl">
      <p class="text-3xl font-bold text-center">
        Benefit of improving your business
      </p>
    </div>

    <img src="/ring.svg" alt="Ornamen" class="absolute z-50 right-0 bottom-0" />
    <img
      src="/ring.svg"
      alt="Ornamen"
      class="absolute z-50 left-0 top-0 rotate-180" />

    <ul
      class="flex bg-primary gap-10 justify-center items-center py-10 px-40 rounded-2xl z-10">
      <li
        v-for="(benefit, i) in benefits"
        :key="i"
        class="flex flex-col items-center gap-2">
        <img
          :src="benefit.imgUrl"
          :alt="benefit.title"
          width="100"
          height="100" />
        <p class="font-semibold text-xl">{{ benefit.title }}</p>
      </li>
    </ul>
  </div>
</template>
