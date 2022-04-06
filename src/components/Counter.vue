<script setup lang="ts">
const props = defineProps<{
  initial: number
}>()

const { count, inc, dec } = useCounter(props.initial)
</script>

<template>
  <div flex="~ justify-center items-center">
    <div flex rounded justify-center cursor-pointer items-center border-1 p-l-4 p-r-4 w-10>
      {{ count }}
    </div>
    <button class="btn" cursor-pointer m-l-2 m-r-2 @click="inc()">
      +
    </button>
    <button class="btn" cursor-pointer @click="dec()">
      -
    </button>
  </div>
</template>
