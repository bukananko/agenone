<script setup lang="ts">
import { achievements } from "@/constant";
</script>

<template>
  <section
    id="about"
    class="md:px-40 px-3 py-20 bg-primary-500/15 space-y-20 relative">
    <h1 class="text-3xl md:text-5xl font-semibold">
      We are passionate about helping businesses grow and succeed in the digital
      age. We take pride in our work and strive to exceed your expectations
      every time.
    </h1>

    <img
      src="/achievement/circle.svg"
      alt="Ornament"
      class="absolute -top-10 -left-10 md:left-24" />
    <img
      src="/achievement/vectorline.svg"
      alt="Ornament"
      class="absolute max-md:top-44 md:bottom-0 right-0 max-md:left-0 z-[-1]" />

    <div
      class="md:flex max-md:space-y-10 justify-between p-10 bg-primary rounded-2xl text-white z-40">
      <div
        v-for="(achievement, i) in achievements"
        :key="i"
        class="text-center space-y-3">
        <h5 class="text-6xl font-bold">{{ achievement.total }}</h5>
        <p class="text-xl font-semibold">{{ achievement.title }}</p>
      </div>
    </div>
  </section>
</template>
