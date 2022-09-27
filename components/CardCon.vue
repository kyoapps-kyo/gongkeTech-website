<template>
  <div
    class="col-span-2 h-[490px] w-full box-border px-[16px] pt-[30px] pb-[40px] lg:px-[138px] lg:pt-[101px] lg:pb-[70px] flex flex-col justify-start tracking-wide text-white"
  >
    <h3 class="text-[12px] lg:text-[16px] font-bold mb-6 lg:mb-8">
      <slot name="subtitle">xxx</slot>
    </h3>
    <h2 class="text-[27px] lg:text-[32px] font-bold mb-4 lg:mb-6">
      <slot name="title">xxx</slot>
    </h2>
    <p class="grow text-[16px] font-bold mb-8">
      <slot name="description">xxx</slot>
    </p>
    <MoreBtn class="self-center" bg-class="bg-black text-white" />
  </div>
</template>
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
