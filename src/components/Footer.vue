<script setup lang="ts">

const activeClass = 'text-teal-600'

const navList = [
  {
    icon: 'i-carbon-home',
    path: '/',
  },
  {
    icon: 'i-carbon-cube',
    path: '/cube',
  }, {
    icon: 'i-carbon-chat-bot',
    path: '/chat',
  },
  {
    icon: 'i-carbon-user',
    path: '/user',
  },
]

</script>

<template>
  <nav w-screen text-xl mt-2 flex gap-2 justify-around fixed bottom-0 left-0>
    <router-link v-for="(item,index) in navList" :key="index" :to="item.path" class="icon-btn !outline-none p-2" :active-class="activeClass">
      <div :class="item.icon" />
    </router-link>
    <!-- <a
      class="icon-btn !outline-none p-2 "
      i-carbon-logo-github
      rel="noreferrer"
      href="https://github.com/antfu/vitesse-lite"
      target="_blank"
      title="GitHub"
    /> -->
  </nav>
</template>
