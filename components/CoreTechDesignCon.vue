<template>
  <div class="grid lg:grid-cols-2 h-screen lg:h-[680px]" :class="bgClass">
    <div
      class="h-[30vh] w-full lg:h-[400px] lg:w-[400px] flex justify-center items-center lg:m-auto"
    >
      <slot name="img"></slot>
    </div>
    <div
      class="m-auto h-[70vh] w-full lg:h-[680px] lg:w-full flex flex-col lg:justify-center justify-start items-start px-6 lg:px-0"
    >
      <h6 class="text-black mb-[38px]"><slot name="number"></slot></h6>
      <h4 class="text-black mb-[56px]">
        <slot name="title"></slot>
      </h4>
      <p
        class="text-description w-full lg:w-[610px] text-center"
        style="color: black"
      >
        <slot></slot>
      </p>
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps({
  bgClass: {
    type: String,
    default: '',
  },
})
</script>
