<template>
  <div class="flex items-center justify-between">
    <div flex="~ gap-2">
      <button
        class="border rounded px-2 py-1"
        @click="count -= 1"
      >
        -
      </button>
      <span>{{ count }}</span>
      <button
        class="border rounded px-2 py-1"
        @click="count += 1"
      >
        +
      </button>
    </div>
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps<{
  count?: number
}>()

const count = ref(props.count || 0)
</script>
