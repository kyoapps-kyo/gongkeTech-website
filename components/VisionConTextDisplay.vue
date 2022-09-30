<template>
  <div class="text-[24px] lg:text-[34px] w-full lg:w-[1200px] mx-auto">
    <div
      ref="target"
      class="transition-all duration-1000"
      :style="`opacity: ${opacity}`"
    >
      <p class="">
        <slot></slot>
      </p>
      <div class="w-full overflow-hidden">
        <h3 class="mb-[20px] lg:mb-[41px]">
          <slot name="title"></slot>
        </h3>
        <p class="text-detail leading-[2.0] w-full lg:float-right lg:w-[900px]">
          <slot name="content"></slot>
        </p>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref, computed } from 'vue'
import { useElementBounding, useWindowSize } from '@vueuse/core'
const target = ref(null)
const { top, bottom } = useElementBounding(target)
const { height } = useWindowSize()
const opacity = computed(() => {
  if (top.value / height.value < 1 / 2 && bottom.value / height.value > 1 / 2)
    return 1
  else return 0.2
})
</script>

<style scoped></style>
