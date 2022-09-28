<!-- 给more-btn传一个link过去，指向product页面 -->
<template>
  <div class="lg:grid lg:grid-cols-2">
    <div
      class="h-[30vh] lg:h-screen w-full bg-black text-white px-[16px] lg:px-[114px] pt-10 lg:pt-0 flex flex-col justify-center lg:items-end"
    >
      <div class="">
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
      class="h-[70vh] lg:h-screen w-full bg-white lg:pl-[107px] flex items-center"
    >
      <slot name="product-img"> </slot>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    link: {
      type: String,
      default: '/',
    },
    btnShow: {
      type: String,
      default: 'true',
    },
  },
})
</script>
