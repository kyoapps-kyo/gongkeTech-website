<template>
  <header
    ref="target"
    class="header fixed top-0 h-[48px] lg:h-[58px] w-full bg-black bg-opacity-60 transition-opacity duration-1000"
    :class="isShow ? '' : 'opacity-0'"
  >
    <div
      class="container mx-auto flex justify-between items-center h-full px-4 lg:px-0"
    >
      <Logo show-logo="true" show-text="true" />
      <Navigation />
    </div>
  </header>
</template>
<script lang="ts" setup>
import { useMouseInElement, useWindowScroll } from '@vueuse/core'
import { computed, ref } from 'vue'
const target = ref<HTMLElement | null>(null)
const { elementY } = useMouseInElement(target)
const { y } = useWindowScroll()
const isShow = computed(() => {
  if (y.value < 240 || elementY.value < 180) return true
  else return false
})
</script>
