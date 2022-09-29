<template>
  <main
    class="bg-white w-screen h-full pt-0 lg:pt-[120px] pb-[20px] lg:pb-[40px]"
  >
    <div class="new-con container mx-auto pb-[20px] lg:pb-[71px]">
      <h2 class="text-[24px] font-bold text-center mb-[40px] lg:mb-[83px]">
        新闻资讯
      </h2>
      <div class="lg:grid lg:grid-cols-2 lg:gap-x-[115px]">
        <NewsUpdate />
        <NewsRelease />
      </div>
      <div class="w-full"></div>
      <MoreBtn bg-class="bg-black text-white mx-auto mt-[20px] lg:mt-[72px]" />
    </div>
  </main>
</template>
