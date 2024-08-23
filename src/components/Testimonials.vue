<script setup lang="ts">
import { testimonials } from "@/constant";
import { Icon } from "@iconify/vue";
</script>

<template>
  <section class="md:px-40 px-3 relative overflow-hidden">
    <div class="space-y-5 md:columns-2 relative">
      <div
        v-for="(testimonial, i) in testimonials"
        :key="i"
        class="rounded-2xl p-3 bg-gray-100 odd:bg-primary odd:text-white space-y-3 w-fit group -translate-y-28 md:-translate-y-10">
        <p class="font-semibold group-even:text-gray-500">
          {{ testimonial.desc }}
        </p>

        <div class="flex items-center gap-2">
          <img
            :src="testimonial.imgUrl"
            alt="Testimonial"
            class="size-11 rounded-full" />

          <div>
            <p class="font-bold">{{ testimonial.name }}</p>
            <p>{{ testimonial.job }}</p>
          </div>
        </div>
      </div>
    </div>

    <div
      class="flex max-md:gap-5 flex-col md:flex-row justify-between items-center bg-dark text-white md:px-20 py-10 md:rounded-t-[5rem] absolute bottom-0 right-0 md:right-20 left-0 md:left-20 rounded-t-[3rem] max-md:mx-3">
      <p class="text-2xl md:text-5xl font-bold max-md:text-center">
        Let's discuss and bring your <br class="max-md:hidden" />
        vision to life.
      </p>

      <button
        class="flex justify-center items-center bg-primary rounded-full py-3 px-4">
        Lets Talk <Icon icon="tabler:arrow-right" width="20" class="ml-1" />
      </button>
    </div>
  </section>
</template>
