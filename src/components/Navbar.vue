<script setup lang="ts">
import { navbar } from "@/constant";
import { Icon } from "@iconify/vue";
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuTrigger,
} from "@/components/ui/dropdown-menu";
</script>

<template>
  <header
    class="flex justify-between items-center md:py-3 p-6 md:px-20 bg-dark text-white sticky top-0 right-0 left-0 z-50">
    <div class="flex justify-center items-center gap-2">
      <img src="/logo.svg" alt="Agenone" width="52" height="52" />
      <p class="font-bold italic text-lg">Agenone</p>
    </div>

    <ul class="hidden md:flex justify-center items-center gap-10">
      <li v-for="(nav, i) in navbar" :key="i">
        <a :href="nav.href">{{ nav.title }}</a>
      </li>
    </ul>

    <button
      class="bg-primary py-2 px-4 rounded-full font-semibold max-md:hidden">
      Contact Us
    </button>

    <DropdownMenu>
      <DropdownMenuTrigger class="md:hidden">
        <Icon icon="solar:hamburger-menu-broken" width="32" />
      </DropdownMenuTrigger>

      <DropdownMenuContent class="bg-primary mr-5 py-5 px-2 text-white">
        <DropdownMenuItem v-for="(nav, i) in navbar" :key="i">
          <a :href="nav.href">{{ nav.title }}</a>
        </DropdownMenuItem>
      </DropdownMenuContent>
    </DropdownMenu>
  </header>
</template>
