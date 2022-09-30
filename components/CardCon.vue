<template>
  <div
    ref="target"
    class="col-span-2 h-[490px] w-full box-border px-[16px] pt-[30px] pb-[40px] lg:px-[138px] lg:pt-[101px] lg:pb-[70px] flex flex-col justify-start tracking-wide text-white"
    :style="{
      transform: cardTransform,
      transition: 'transform 0.25s ease-out',
    }"
  >
    <h5 class="mb-6 lg:mb-8">
      <slot name="subtitle">xxx</slot>
    </h5>
    <h3 class="mb-4 lg:mb-6">
      <slot name="title">xxx</slot>
    </h3>
    <p class="grow text-detail mb-8">
      <slot name="description">xxx</slot>
    </p>
    <MoreBtn class="self-center" bg-class="bg-black text-white" />
  </div>
</template>
<script lang="ts" setup>
import { ref, computed } from 'vue'
import { useMouseInElement } from '@vueuse/core'

const target = ref(null)

const { elementX, elementY, isOutside, elementHeight, elementWidth } =
  useMouseInElement(target)

const cardTransform = computed(() => {
  const MAX_ROTATION = 6

  const rX = (
    MAX_ROTATION / 2 -
    (elementY.value / elementHeight.value) * MAX_ROTATION
  ).toFixed(2)

  const rY = (
    (elementX.value / elementWidth.value) * MAX_ROTATION -
    MAX_ROTATION / 2
  ).toFixed(2)
  return isOutside.value
    ? ''
    : `perspective(${elementWidth.value}px) rotateX(${rX}deg) rotateY(${rY}deg)`
})
</script>
<style scoped>
.vision-card {
  background: url(@/assets/images/vision-card-bg.jpg) no-repeat center center /
    cover;
  /* filter: brightness(0.9); */
}
.tech-card {
  background: url(@/assets/images/tech-card-bg.jpg) no-repeat center center /
    cover;
  /* filter: brightness(0.9); */
}
</style>
