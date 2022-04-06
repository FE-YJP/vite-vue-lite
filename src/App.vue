<script setup lang="ts">
const route = useRoute()
const nav_list = [
  '/', '/cube', '/chat', '/user',
]

const showNav = ref(true)

watch(route, (newval, oldval) => {
  if (nav_list.includes(newval.path))
    showNav.value = true
  else
    showNav.value = false
})

</script>
<template>
  <main text="center gray-700 dark:gray-200" flex="~ col " w-screen h-screen>
    <Head />
    <router-view v-slot="{ Component }" h-screen>
      <transition name="fade">
        <component :is="Component" flex-1 h-screen />
      </transition>
    </router-view>
    <Footer v-show="showNav" />
  </main>
</template>
<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity .5s ease;
  position: fixed;
  width: 100vw;
  height: 100vh;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  position: fixed;
  width: 100vw;
  height: 100vh;
}
</style>
