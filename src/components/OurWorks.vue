<script setup lang="ts">
import { services } from "@/constant";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
</script>

<template>
  <section
    id="project"
    class="md:px-40 px-3 py-20 bg-dark relative text-white space-y-10">
    <img
      src="/ourworks/circle1.svg"
      alt="ornament"
      class="absolute -top-32 md:top-0 left-0 max-md:size-1/2" />
    <img
      src="/ourworks/circle1.svg"
      alt="ornament"
      class="absolute -bottom-10 md:bottom-0 right-0 max-md:w-1/2 rotate-180" />

    <div>
      <h1 class="text-5xl font-bold text-center">
        Our Project Have Been
        <span class="text-transparent bg-clip-text bg-primary">Done</span>
      </h1>
      <p class="text-center text-gray-400">
        Take a look at some of our recent projects and see how we've helped
        other businesses elevate their brand and drive business growth.
      </p>
    </div>

    <Tabs
      default-value="item1"
      class="flex justify-center items-center flex-col space-y-10">
      <TabsList class="max-md:w-full">
        <TabsTrigger
          v-for="(service, i) in services"
          :key="i"
          :value="service.value">
          {{ service.title }}
        </TabsTrigger>
      </TabsList>

      <TabsContent value="item1">
        <div class="md:w-96 md:h-max bg-[#202020] p-3 rounded-2xl">
          <div class="space-y-3">
            <div
              class="rounded-2xl overflow-hidden relative group hover:cursor-pointer">
              <img
                src="/uiux.png"
                alt="apaja"
                class="size-full aspect-square bg-contain group-hover:opacity-60 transition-all duration-200" />

              <img
                src="/hoverarrow.png"
                alt="Arrow"
                class="size-1/3 absolute top-1/2 scale-0 group-hover:scale-100 translate-x-full translate-y-72 group-hover:-translate-y-1/2 transition-all duration-300 ease-in-out transform" />
            </div>

            <h3>Title</h3>
            <p class="text-gray-400">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Doloremque, explicabo!
            </p>
          </div>
        </div>
      </TabsContent>
    </Tabs>
  </section>
</template>
