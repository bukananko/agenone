<script setup lang="ts">
import { services } from "@/constant";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import {
  Card,
  CardContent,
  CardDescription,
  CardTitle,
} from "@/components/ui/card";
</script>

<template>
  <section class="md:px-40 px-3 py-20 bg-dark relative text-white space-y-10">
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
      <TabsList class="flex max-md:w-full">
        <TabsTrigger
          v-for="(service, i) in services"
          :key="i"
          :value="service.value">
          {{ service.title }}
        </TabsTrigger>
      </TabsList>

      <TabsContent value="item1">
        <Card class="md:w-1/2">
          <CardContent class="space-y-3">
            <div
              class="rounded-2xl overflow-hidden relative group hover:cursor-pointer">
              <img
                src="/uiux.png"
                alt="apaja"
                class="w-full h-full aspect-square bg-contain group-hover:opacity-60 transition-all duration-200" />

              <img
                src="/hoverarrow.png"
                alt="Arrow"
                class="size-1/3 absolute top-1/2 scale-0 group-hover:scale-100 translate-x-full translate-y-72 group-hover:-translate-y-1/2 transition-all duration-300 ease-in-out transform" />
            </div>

            <CardTitle>Title</CardTitle>

            <CardDescription class="text-gray-400">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Id dicta
              aperiam cumque odio asperiores assumenda quaerat earum. Natus enim
              incidunt modi doloremque laudantium ducimus sint. Nisi laudantium
              quis odit minima nesciunt architecto nemo a optio alias iusto,
              repudiandae esse enim similique. Nostrum sequi commodi rem
              perspiciatis ratione nihil libero atque facilis ea quibusdam
              fugiat aliquid repudiandae veniam ullam magnam asperiores
              eligendi, quidem necessitatibus nesciunt aut maiores totam
              sapiente enim? Maxime itaque ipsum ducimus ut quae alias corporis
              commodi nesciunt recusandae nobis! Consequatur magni vel neque
              amet illo, reiciendis aperiam nam praesentium iure nesciunt non,
              placeat commodi quisquam itaque voluptatibus alias.
            </CardDescription>
          </CardContent>
        </Card>
      </TabsContent>
    </Tabs>
  </section>
</template>
