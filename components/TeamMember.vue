<template>
  <div
    class="w-[120px h-[227px] lg:w-[180px] lg:h-[277px] flex flex-col justify-between items-center"
  >
    <div
      class="radius-full w-[180px] h-[180px] overflow-hidden flex justify-center items-center"
    >
      <slot name="avatar"></slot>
    </div>
    <h4 class="text-black text-center">
      <slot name="name"></slot>
    </h4>
    <p class="text-detail text-center" style="color: black">
      <slot></slot>
    </p>
  </div>
</template>
