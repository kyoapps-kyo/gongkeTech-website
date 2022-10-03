<template>
  <div>
    <OtherBanner class="tech-banner">
      <template slot="subtitle">技术支持</template>
      <template slot="title">关键词关键词关键词关键词关键词</template>
      <template slot="description">简述简述简述简述简述简述简述简述</template>
    </OtherBanner>
    <section class="core-tech w-screen py-10 lg:py-24">
      <h3 class="text-center mb-6 lg:mb-20">核心技术</h3>
      <div class="container mx-auto grid lg:grid-cols-2">
        <div
          class="flex justify-center items-center bg-[#d9d9d9] h-[50vh] tech1"
        >
          <h3 class="drop-shadow-[2px_2px_2px_rgba(0,0,0,1)]">技术一</h3>
        </div>
        <div
          class="flex flex-col justify-center items-center min-h-[50vh] gap-4 lg;gap-8 px-6 lg:px-0 py-6 lg:py-0"
        >
          <h4 class="hidden lg:block">技术一</h4>
          <p class="text-detail lg:w-[525px]">
            文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
          </p>
        </div>
        <div
          class="flex justify-center items-center bg-[#d9d9d9] h-[50vh] tech2 lg:order-last"
        >
          <h3 class="drop-shadow-[2px_2px_2px_rgba(0,0,0,1)]">技术二</h3>
        </div>
        <div
          class="flex flex-col justify-center items-center min-h-[50vh] gap-4 lg;gap-8 px-6 lg:px-0 py-6 lg:py-0"
        >
          <h4 class="hidden lg:block">技术二</h4>
          <p class="text-detail lg:w-[525px]">
            文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
          </p>
        </div>
      </div>
    </section>
    <section class="core-tech1 w-screen py-4 lg:py-12 bg-[#f7f7f7]">
      <div class="container mx-auto px-6 lg:px-20">
        <h5 class="text-black mb-6 lg:mb-10">技术总结</h5>
        <p class="text-detail mb-6 lg:mb-10" style="color: black">
          描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字
        </p>
        <div
          class="bg-gray-200 max-w-[1100px] mx-auto h-[180px] lg:h-[500px] relative mb-16 lg:mb-28"
        >
          <p
            class="iconfont text-black text-[50px] hover:text-white hover:scale-[1.2] cursor-pointer transform transition-all duration-500 absolute top-1/2 left-1/2 mt-[-37.5px] ml-[-25px]"
          >
            &#xe624;
          </p>
        </div>
      </div>
    </section>
    <section class="tech-tips w-screen py-10 lg:py-24 bg-[#ffffff]">
      <h5 class="text-center text-black mb-8 lg:mb-20">技术特点</h5>
      <div class="container mx-auto px-6 lg:px-20">
        <TechSelectCard />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '技术支持',
    }
  },
}
</script>

<style scoped>
.tech1 {
  background: url(@/assets/images/core-tech-bg1.jpg) no-repeat center center /
    cover;
}
.tech2 {
  background: url(@/assets/images/core-tech-bg2.jpg) no-repeat center center /
    cover;
}
</style>
