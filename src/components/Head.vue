<script setup lang="ts">
import { isDark, toggleDark } from '~/composables'
onMounted(() => {

})
</script>
<template>
  <div w-screen h-10 fixed top-0>
    <button class="icon-btn !outline-none p-2 text-xl" fixed right-0 @click="toggleDark()">
      <div v-if="isDark" i-carbon-moon />
      <div v-else i-carbon-sun />
    </button>
  </div>
</template>

<style scoped>

</style>
