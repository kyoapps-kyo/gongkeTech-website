<!-- 给more-btn传一个link过去，指向product页面
除了第一个之后的都不要背景，noBgColor
-->
<template>
  <div ref="el" class="lg:grid lg:grid-cols-2">
    <div
      class="h-[30vh] lg:h-screen w-full text-white px-[16px] lg:px-[114px] pt-[96px] lg:pt-0 flex flex-col justify-center lg:items-end"
    >
      <div
        class=""
        :style="`opacity: ${opacity}; transform: translateY(-${
          process * 20
        }px);`"
      >
        <h4 class="font-bold text-[16px] lg:text-[24px] lg:mb-8">
          <slot name="subtitle"></slot>
        </h4>
        <h3
          class="font-bold text-[27px] lg:text-[36px] mb-2 lg:mb-20 lg:w-[463px]"
        >
          <slot name="title"></slot>
        </h3>
        <p class="text-[16px] lg:text-[24px] mb-2 lg:mb-32 lg:w-[463px]">
          <slot name="description"></slot>
        </p>
        <div class="w-full">
          <MoreBtn
            v-if="btnShow === 'true'"
            class="mx-auto lg:mx-0"
            bg-class="bg-white text-black"
            :link="link"
          />
        </div>
      </div>
    </div>
    <div
      class="h-[70vh] lg:h-screen w-full lg:pl-[107px] flex items-center"
      :class="noBgColor ? 'bg-none' : 'bg-white'"
    >
      <div
        :style="`opacity: ${opacity}; transform: translateY(-${
          process * 20
        }px);`"
      >
        <slot name="product-img"> </slot>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { ref, onMounted, computed } from 'vue'
import { useWindowScroll, useElementSize } from '@vueuse/core'
const props = defineProps({
  link: {
    type: String,
    default: '/',
  },
  btnShow: {
    type: String,
    default: 'true',
  },
  noBgColor: {
    type: Boolean,
    default: true,
  },
})
const el = ref<HTMLElement | null>(null)
const elTop = ref<number | undefined>(0)
const { y } = useWindowScroll()
const { height } = useElementSize(el)
const MAX_OPACITY = 2
const process = computed(() => {
  return 1 - ((elTop.value - y.value) / height.value).toFixed(2)
})
const opacity = computed(() => {
  if (process.value < 1.4)
    // 如果传进来的是第一个proinfo，直接设置透明度为1
    return props.noBgColor
      ? (Math.max(0.99, process.value) - 0.99) * MAX_OPACITY
      : (Math.max(0.2, process.value) - 0.2) * MAX_OPACITY
  else return -(Math.min(1.99, process.value) - 1.99) * MAX_OPACITY * 2
})

onMounted(() => {
  elTop.value = el.value?.offsetTop
})
</script>
