<template>
  <section class="banner w-full h-screen">
    <div class="container mx-auto relative h-screen">
      <div
        ref="target"
        class="banner-con flex flex-col items-start h-full lg:h-fit lg:w-[920px] pt-24 px-8 lg:py-10 lg:px-10 bg-black/50 lg:bg-black/30 backdrop-blur-sm lg:absolute lg:top-1/2 lg:mt-[-320px] lg:rounded-lg"
        :style="{
          transform: cardTransform,
          transition: 'transform 0.25s ease-out',
        }"
      >
        <div class="slogan mb-8 lg:mb-[82px]">
          <nuxt-img
            :src="$t('pages.index.banner.sloganSrc')"
            sizes="md:200px xxl:400px"
          />
        </div>
        <div
          class="banner-description text-[18px] lg:text-[24px] text-white leading-loose"
        >
          {{ $t('pages.index.banner.content') }}
        </div>
      </div>
      <div
        class="absolute top-[450px] right-1/2 mr-[-48px] lg:mr-0 lg:top-1/2 lg:mt-[-230px] lg:right-[260px]"
      >
        <PlayBtn />
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
import PlayBtn from './PlayBtn.vue'

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
  background: #000 url('@/assets/images/banner-bg.jpg') no-repeat center center /
    auto 100%;
  background-blend-mode: hard-light;
  filter: saturate(30%);
  background-attachment: fixed;
}
</style>
