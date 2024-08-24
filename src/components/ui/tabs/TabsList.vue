<script setup lang="ts">
import { type HTMLAttributes, computed } from 'vue'
import { TabsList, type TabsListProps } from 'radix-vue'
import { cn } from '@/lib/utils'

const props = defineProps<TabsListProps & { class?: HTMLAttributes['class'] }>()

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props

  return delegated
})
</script>

<template>
  <TabsList
    v-bind="delegatedProps"
    :class="cn(
      'flex flex-wrap gap-x-5 w-fit h-fit items-center justify-center p-3 bg-white rounded-2xl md:rounded-full text-gray-500 z-40',
      props.class,
    )"
  >
    <slot />
  </TabsList>
</template>
