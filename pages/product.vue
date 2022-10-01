<template>
  <div>
    <section class="product-banner bg-white">
      <div
        class="container mx-auto text-center pt-[50px] lg:pt-[90px] pb-[20px] lg:pb-[34px]"
      >
        <div class="px-4 lg:px-0">
          <h2 class="text-black mb-[10px] lg:mb-[25px]">产品名称</h2>
          <p class="text-detail lg:mb-[70px] mb-[30px]" style="color: black">
            产品说明产品说明产品说明产品说明产品说明产品说明产
          </p>
        </div>
        <div
          class="banner h-[490px] w-full flex flex-col lg:flex-row justify-center items-center gap-4 lg:gap-20 px-4 lg:px-0 lg:mb-[40px] mb-[20px]"
        >
          <p
            class="text-description leading-[40px] lg:leading-[60px] w-full lg:w-[655px] lg:text-left font-bold"
            style="color: black; text-shadow: 1px 1px 2px white"
          >
            介绍介绍介绍介绍介绍绍介绍介绍介绍介绍绍介绍介绍介绍介绍绍介绍介绍介绍介绍绍介绍介绍介绍介绍
          </p>
          <PlayBtn />
        </div>
        <p
          class="text-description lg:w-[890px] mx-auto px-4 lg:px-0"
          style="color: black"
        >
          介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介绍文字介
        </p>
      </div>
    </section>
    <section
      class="use-case bg-[#f7f7f7] pt-[40px] lg:pt-[55px] pb-[70px] lg:pb-[90px]"
    >
      <div class="container mx-auto text-center">
        <h5 class="text-[#aaa] mb-[18px] lg:mb-[21px]">USE CASE</h5>
        <h3 class="text-black mb-[34px] lg:mb-[44px]">产品使用案例</h3>
        <div class="lg:flex justify-around items-center mb-[50px] lg:mb-[62px]">
          <UseCaseCard />
          <UseCaseCard />
          <UseCaseCard />
        </div>
        <div class="w-full">
          <MoreBtn bg-class="bg-black text-white mx-auto" />
        </div>
      </div>
    </section>
    <section class="step-list w-full py-20 relative">
      <h3 class="text-black text-center mb-8">设定步骤</h3>
      <div class="container mx-auto">
        <StepListOption before-con="1">
          step a
          <template slot="content-video"></template>
          <template slot="content-detail"
            >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
          >
        </StepListOption>
        <StepListOption before-con="2">
          step a
          <template slot="content-video"></template>
          <template slot="content-detail"
            >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
          >
        </StepListOption>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '产品信息',
    }
  },
}
</script>
<style scoped>
.product-banner .banner {
  background: url(@/assets/images/product-card-bg.jpg) no-repeat center center/
    cover;
}
.step-list::before {
  content: '';
  width: 100%;
  height: 100%;
  position: absolute;
  top: -5rem;
  z-index: -1;
  background: #fff url(@/assets/images/step-list-bg.jpg) no-repeat center
    center/ 100% 100vh;
  background-attachment: fixed;
  filter: brightness(140%) contrast(60%) saturate(70%);
}
</style>
