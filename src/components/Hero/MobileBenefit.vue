<script setup lang="ts">
import { benefits } from "@/constant";
import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from "@/components/ui/carousel";
</script>

<template>
  <div class="relative flex justify-center items-center md:hidden">
    <div class="absolute -top-10 bg-primary w-72 py-3 rounded-t-2xl z-0">
      <p class="font-bold text-center">Benefit of improving your business</p>
    </div>

    <img src="/ring.svg" alt="Ornament" class="absolute z-50 left-0 -top-10 rotate-180" />

    <Carousel class="w-80 h-max bg-primary rounded-2xl">
      <CarouselContent>
        <CarouselItem v-for="(benefit, i) in benefits" :key="i">
          <div class="gap-2 flex justify-center items-center flex-col py-10">
            <img
              :src="benefit.imgUrl"
              :alt="benefit.title"
              width="100"
              height="100" />
            <p class="font-semibold text-xl">{{ benefit.title }}</p>
          </div>
        </CarouselItem>
      </CarouselContent>

      <CarouselPrevious />
      <CarouselNext />
    </Carousel>
  </div>
</template>
