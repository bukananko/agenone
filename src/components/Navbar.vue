<script setup lang="ts">
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
    class="flex justify-between items-center md:py-3 p-6 md:px-20 bg-transparent sticky top-0 right-0 left-0 bg-dark">
    <div class="flex justify-center items-center gap-2">
      <img src="/logo.svg" alt="Agenone" width="52" height="52" />
      <p class="font-bold italic text-lg">Agenone</p>
    </div>

    <ul class="hidden md:flex justify-center items-center gap-10">
      <li>Home</li>
      <li>Services</li>
      <li>Project</li>
      <li>About Us</li>
    </ul>

    <button
      class="bg-primary py-2 px-4 rounded-full font-semibold max-md:hidden">
      Contact Us
    </button>

    <DropdownMenu>
      <DropdownMenuTrigger class="md:hidden">
        <Icon icon="solar:hamburger-menu-broken" width="32" />
      </DropdownMenuTrigger>

      <DropdownMenuContent class="bg-primary mr-5 py-5 px-2">
        <DropdownMenuItem>
          <a href="#">Home</a>
        </DropdownMenuItem>
        <DropdownMenuItem>
          <a href="#services">Services</a>
        </DropdownMenuItem>
        <DropdownMenuItem>
          <a href="#project">Project</a>
        </DropdownMenuItem>
        <DropdownMenuItem>
          <a href="#about">About Us</a>
        </DropdownMenuItem>
      </DropdownMenuContent>
    </DropdownMenu>
  </header>
</template>
