<template>
  <main
    class="bg-white w-screen h-full pt-0 lg:pt-[120px] pb-[40px] lg:pb-[40px]"
  >
    <div class="new-con container mx-auto pb-[20px] lg:pb-[71px]">
      <h2
        class="text-[24px] font-bold text-center mb-[40px] lg:mb-[83px]"
        :class="color"
      >
        新闻资讯
      </h2>
      <div class="lg:grid lg:grid-cols-2 lg:gap-x-[115px]">
        <NewsUpdate :limit="limit" />
        <NewsRelease :limit="limit" />
      </div>
      <div class="w-full" :class="{ hidden: !show }">
        <MoreBtn
          :link="link"
          bg-class="bg-black text-white mx-auto mt-[50px] lg:mt-[72px]"
        />
      </div>
    </div>
  </main>
</template>

<script lang="ts" setup>
defineProps({
  limit: {
    type: Number,
    default: 5,
  },
  color: {
    type: String,
    default: '',
  },
  show: {
    type: Boolean,
    default: true,
  },
  link: {
    type: String,
    default: '/',
  },
})
</script>
