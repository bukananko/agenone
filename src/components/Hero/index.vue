<script setup lang="ts">
import { Icon } from "@iconify/vue";
import DesktopBenefit from "./DesktopBenefit.vue";
import MobileBenefit from "./MobileBenefit.vue";
</script>

<template>
  <section
    id="hero"
    class="flex justify-center items-center flex-col py-10 md:py-20 gap-20 md:gap-40">
    <div class="flex justify-center items-center flex-col">
      <p class="bg-white/10 py-2 px-3 rounded-full text-xs mb-2">
        NUMBER ONE CREATIVE DIGITAL AGENCY
      </p>

      <div class="px-10 md:mx-60 text-center space-y-3">
        <h1 class="font-bold text-4xl md:text-5xl">
          <span class="text-transparent bg-primary bg-clip-text"
            >Smart Choices</span
          ><br />
          For Your Business Growth
        </h1>

        <p class="text-gray-400">
          We're a team of experienced designers, developers,
          <br class="hidden md:block" />and marketers, passionate about
          delivering exceptional digital solutions.
        </p>
      </div>

      <button
        class="flex justify-center items-center bg-primary rounded-full py-3 px-4 mt-10">
        Contact Us <Icon icon="tabler:arrow-right" width="20" class="ml-1" />
      </button>
    </div>

    <DesktopBenefit />
    <MobileBenefit />
  </section>
</template>
