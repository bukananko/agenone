<script setup lang="ts">
import { services } from "@/constant";
import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from "@/components/ui/accordion";
</script>

<template>
  <section id="services" class="bg-white px-3 md:px-40 py-20">
    <h1 class="text-center text-3xl md:text-5xl font-bold pb-20">
      The Services We Offer
      <span class="text-transparent bg-clip-text bg-primary">For You</span>
    </h1>

    <Accordion
      type="single"
      collapsible
      class="w-full space-y-5"
      default-value="item1">
      <AccordionItem
        v-for="(service, i) in services"
        :key="service.value"
        :value="service.value"
        class="bg-gray-100 px-5 md:px-10 py-2 md:py-5 rounded-2xl">
        <AccordionTrigger>
          <div class="flex gap-2 md:gap-5 text-lg md:text-2xl">
            <p>0{{ i + 1 }}</p>
            <p>{{ service.title }}</p>
          </div>
        </AccordionTrigger>
        <AccordionContent class="space-y-5">
          <p>{{ service.desc }}</p>
          <img :src="service.imgUrl" :alt="service.title" />
        </AccordionContent>
      </AccordionItem>
    </Accordion>
  </section>
</template>
