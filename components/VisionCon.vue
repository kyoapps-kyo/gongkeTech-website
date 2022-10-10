<template>
  <section class="vision-con">
    <div
      class="pt-[20px] lg:pt-[40px] container mx-auto px-4 lg:px-0 text-white"
    >
      <VisionConTextDisplay class="pb-[40px] lg:pb-[80px]">
        <p
          v-for="(item, index) in $t('pages.vision.visionContent.description')"
          :key="item + index"
          class="text-description leading-[40px] lg:leading-[60px]"
        >
          {{ item }}
        </p>
      </VisionConTextDisplay>
      <VisionConTextDisplay
        v-for="(item, index) in $t('pages.vision.visionContent.details')"
        :key="item.title + index"
        class="pb-[40px] lg:pb-[80px]"
      >
        <template slot="title">{{ item.title }}</template>
        <template slot="content">{{ item.content }}</template>
      </VisionConTextDisplay>
    </div>
    <div
      class="container mx-auto transition-all duration-500 opacity-60 translate-y-10 hover:opacity-100 hover:translate-y-0"
    >
      <div
        class="future w-full h-full px-4 lg:px-0 lg:w-[845px] lg:h-[845px] mx-auto text-white text-center pt-[20px] lg:pt-[71px] pb-[60px] lg:pb-[40px] mb-[100px] lg:mb-0"
      >
        <h4>{{ $t('pages.vision.visionContent.future.title') }}</h4>
        <h6 class="mb-[50px] lg:mb-[100px] font-normal">
          FUTURE HISTORY of EVOLUTION
        </h6>
        <p class="text-detail lg:w-[600px] lg:mx-auto lg:mb-[120px] mb-[60px]">
          {{ $t('pages.vision.visionContent.future.detail') }}
        </p>
        <div class="w-full">
          <MoreBtn
            bg-class="bg-white text-black mx-auto"
            :link="$t('pages.vision.visionContent.future.link')"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup></script>

<style scoped>
.future {
  background: #000 url(@/assets/images/future-bg.jpg) no-repeat center center /
    cover;
  background-blend-mode: hard-light;
  filter: saturate(90%);
}
</style>
