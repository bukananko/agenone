<script setup lang="ts">
import { type HTMLAttributes, computed } from "vue";
import {
  AccordionHeader,
  AccordionTrigger,
  type AccordionTriggerProps,
} from "radix-vue";
import { cn } from "@/lib/utils";
import { Icon } from "@iconify/vue";

const props = defineProps<
  AccordionTriggerProps & { class?: HTMLAttributes["class"] }
>();

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props;

  return delegated;
});
</script>

<template>
  <AccordionHeader class="flex">
    <AccordionTrigger
      v-bind="delegatedProps"
      :class="
        cn(
          'flex flex-1 items-center justify-between py-4 font-semibold transition-all [&[data-state=open]]:text-primary-500 [&[data-state=open]>svg]:rotate-90',
          props.class
        )
      ">
      <slot />
      <slot name="icon">
        <Icon
          icon="fluent:arrow-right-12-filled"
          class="shrink-0 transition-transform duration-200"
          width="25" />
      </slot>
    </AccordionTrigger>
  </AccordionHeader>
</template>
