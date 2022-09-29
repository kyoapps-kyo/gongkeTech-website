<template>
  <section class="banner w-full h-screen">
    <div class="container mx-auto relative h-screen">
      <div
        ref="target"
        class="banner-con flex flex-col items-start h-full w-full lg:h-[270px] lg:w-[1200px] pt-24 px-8 lg:py-0 lg:px-0 lg:absolute lg:top-1/3 lg:left-1/2 lg:ml-[-600px] lg:mt-[-150px] text-white"
        :style="{
          transform: cardTransform,
          transition: 'transform 0.25s ease-out',
        }"
      >
        <h4 class="text-[12px] mb-[90px] lg:mb-[72px]">公司愿景</h4>
        <h3
          class="banner-description text-[28px] lg:text-[54px] font-bold text-center w-full mb-[52px] lg:mb-[72px]"
        >
          Lorem Ipsum从西元15世
        </h3>
        <p class="text-[16px] lg:text-[24px] text-center w-full">
          Lorem Ipsum，也称乱数假文或者哑元文本
        </p>
      </div>
      <LookDownIcon
        class="absolute bottom-[30%] text-white left-1/2 text-[40px] ml-[-20px] lg:text-[80px] lg:ml-[-40px]"
      />
    </div>
  </section>
</template>
<script lang="ts" setup>
import { ref, computed } from 'vue'
import { useMouseInElement } from '@vueuse/core'

const target = ref(null)

const { elementX, elementY, isOutside, elementHeight, elementWidth } =
  useMouseInElement(target)

const cardTransform = computed(() => {
  const MAX_ROTATION = 12

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
.banner {
  background: #000 url('@/assets/images/vision-card-bg.jpg') no-repeat center
    center / cover;
  background-blend-mode: hard-light;
  filter: saturate(30%);
  background-attachment: fixed;
}
</style>
