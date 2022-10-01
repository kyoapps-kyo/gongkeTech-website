<template>
  <div>
    <div
      ref="target"
      class="step-card w-[300px] lg:w-[1000px] h-[60px] lg:h-[80px] bg-white relative mx-auto"
      :data-content-before="beforeCon"
      @click="isOpen = !isOpen"
    >
      <p
        class="pl-[50px] text-description leading-[60px] lg:leading-[80px]"
        style="color: black"
      >
        <slot></slot>
      </p>
      <span
        class="iconfont absolute top-1/2 mt-[-20px] right-6 lg:right-8 leading-[40px] lg:leading-[40px] text-[40px] w-[40px] h-[40px] cursor-pointer transform transition-transform duration-500"
        :class="isOpen ? 'rotate-45' : 'rotate-0'"
      >
        &#xe6df;
      </span>
    </div>
    <transition name="content">
      <div
        v-if="isOpen"
        class="w-[300px] lg:w-[1020px] lg:px-[138px] px-4 bg-white relative lg:left-[-10px] box-border mx-auto"
      >
        <transition name="content">
          <div
            v-show="isOpen"
            class="bg-gray-200 w-full relative mb-6 lg:mb-10 h-[180px] lg:h-[300px]"
          >
            <p
              class="iconfont text-black text-[50px] hover:text-white hover:scale-[1.2] cursor-pointer transform transition-all duration-500 absolute top-1/2 left-1/2 mt-[-37.5px] ml-[-25px]"
            >
              &#xe624;
            </p>
            <slot name="content-video"></slot>
          </div>
        </transition>
        <p class="text-detail pb-10" style="color: black">
          <slot name="content-detail"></slot>
        </p>
      </div>
    </transition>
  </div>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue'
import { useMouseInElement, useMousePressed } from '@vueuse/core'

const target = ref<HTMLElement | null>(null)
const { pressed } = useMousePressed()
const { isOutside } = useMouseInElement(target)
const isOpen = ref<Boolean>(false)
defineProps({
  beforeCon: { type: String, default: '' },
})
</script>

<style scoped>
.step-card::before {
  content: attr(data-content-before);
  position: absolute;
  border-radius: 50%;
  top: 50%;
  margin-top: -35px;
  left: -35px;
  height: 70px;
  width: 70px;
  line-height: 70px;
  font-size: 32px;
  background-color: white;
  text-align: center;
}

.content-enter-active,
.content-leave-active {
  transition: all 1s ease-in-out 0.1s;
  height: 744px;
}
.content-enter,
.content-leave-to {
  /* opacity: 0; */
  height: 0px;
}

@media (min-width: 1024px) {
  .step-card::before {
    margin-top: -47.5px;
    left: -47.5px;
    height: 95px;
    width: 95px;
    line-height: 95px;
    font-size: 40px;
  }
}
</style>
