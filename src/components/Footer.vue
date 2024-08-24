<script setup lang="ts">
import { menu } from "@/constant";
</script>

<template>
  <footer class="md:px-32 px-3 bg-dark text-gray-400 relative">
    <img
      src="/footer/circle1.svg"
      alt="ornament"
      class="absolute top-0 left-0 max-md:w-1/3" />
    <img
      src="/footer/circle2.svg"
      alt="ornament"
      class="absolute bottom-0 right-0 max-md:w-1/2 z-10" />

    <div
      class="flex max-md:flex-col max-md:gap-10 justify-between border-y border-y-gray-600 py-20">
      <div class="space-y-5 md:w-1/2">
        <div class="flex items-center gap-2">
          <img src="/logo.svg" alt="Agenone" class="size-12" />
          <p class="text-xl font-bold italic text-white">Agenone</p>
        </div>

        <p>
          We're a team of experienced designers, developers, and marketers,
          passionate about delivering exceptional digital solutions.
        </p>
        <p>hello@agenone.com</p>
      </div>

      <div class="flex flex-wrap gap-20 z-40">
        <ul class="space-y-3">
          <h5 class="text-white font-semibold">Menu</h5>
          <li v-for="(nav, i) in menu" :key="i">
            <a :href="nav.href">{{ nav.title }}</a>
          </li>
        </ul>

        <ul class="space-y-3">
          <h5 class="text-white font-semibold">Support</h5>
          <li>Faq</li>
          <li>Privacy Policy</li>
          <li>Terms of Service</li>
        </ul>

        <ul class="space-y-3">
          <h5 class="text-white font-semibold">Social Media</h5>
          <li>X</li>
          <li>Linked in</li>
          <li>Instagram</li>
        </ul>
      </div>
    </div>

    <div class="py-5">
      <p class="text-center">
        Copyright © 2023 by Agenone. All rights reserved.
      </p>
    </div>
  </footer>
</template>
