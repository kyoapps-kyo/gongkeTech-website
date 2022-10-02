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
      <div class="container mx-auto flex flex-col pb-20 gap-10">
        <ClickDisplayList before-con="1">
          step a
          <template slot="content-video"></template>
          <template slot="content-detail"
            >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
          >
        </ClickDisplayList>
        <ClickDisplayList before-con="2">
          step b
          <template slot="content-video"></template>
          <template slot="content-detail"
            >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
          >
        </ClickDisplayList>
        <ClickDisplayList before-con="3">
          step c
          <template slot="content-video"></template>
          <template slot="content-detail"
            >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
          >
        </ClickDisplayList>
      </div>
    </section>
    <section class="merit bg-white w-screen">
      <div class="container mx-auto px-4 lg:px-18 pt-16 lg:py-20">
        <h3 class="text-black text-center mb-20">优点说明</h3>
        <div
          class="bg-gray-200 max-w-[1100px] mx-auto h-[180px] lg:h-[500px] relative mb-16 lg:mb-28"
        >
          <p
            class="iconfont text-black text-[50px] hover:text-white hover:scale-[1.2] cursor-pointer transform transition-all duration-500 absolute top-1/2 left-1/2 mt-[-37.5px] ml-[-25px]"
          >
            &#xe624;
          </p>
        </div>
        <p
          class="text-description max-w-[947px] mx-auto mb-8 lg:mb-10"
          style="color: black"
        >
          说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本
        </p>
        <p class="text-detail max-w-[947px] mx-auto" style="color: black">
          说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本说明文本
        </p>
      </div>
    </section>
    <section class="core-tech w-screen bg-[#f7f7f7]">
      <div class="container mx-auto py-20">
        <h3 class="text-black text-center">核心技术</h3>
        <div class="core-tech-con">
          <CoreTechDesignCon class="sticky top-0" bg-class="bg-[#f7f7f7]">
            <template slot="img">
              <nuxt-img
                src="core-tech-bg1.jpg"
                sizes="sm:300px xxl:600px"
              ></nuxt-img>
            </template>
            <template slot="number">核心技术一</template>
            <template slot="title">核心技术标题标题标题</template>
            <span>
              文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本
            </span>
          </CoreTechDesignCon>
          <CoreTechDesignCon class="sticky top-0" bg-class="bg-[#f7f7f7]">
            <template slot="img">
              <nuxt-img
                src="core-tech-bg2.jpg"
                sizes="sm:300px xxl:600px"
              ></nuxt-img>
            </template>
            <template slot="number">核心技术二</template>
            <template slot="title">核心技术标题标题标题</template>
            <span>
              文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本
            </span>
          </CoreTechDesignCon>
        </div>
      </div>
    </section>
    <section class="core-design w-screen bg-[#D9D9D9]">
      <div class="container mx-auto py-20">
        <h3 class="text-black text-center mb-8 lg:mb-[44px]">设计理念</h3>
        <p class="text-detail text-center" style="color: black">
          文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文
        </p>
        <div class="core-tech-con">
          <CoreTechDesignCon class="sticky top-0" bg-class="bg-[#D9D9D9]">
            <template slot="img">
              <nuxt-img
                src="core-tech-bg1.jpg"
                sizes="sm:300px xxl:600px"
              ></nuxt-img>
            </template>
            <template slot="number">核心设计一</template>
            <template slot="title">核心设计标题标题标题</template>
            <span>
              文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本
            </span>
          </CoreTechDesignCon>
          <CoreTechDesignCon class="sticky top-0" bg-class="bg-[#D9D9D9]">
            <template slot="img">
              <nuxt-img
                src="core-tech-bg2.jpg"
                sizes="sm:300px xxl:600px"
              ></nuxt-img>
            </template>
            <template slot="number">核心设计二</template>
            <template slot="title">核心设计标题标题标题</template>
            <span>
              文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本
            </span>
          </CoreTechDesignCon>
        </div>
      </div>
    </section>
    <section class="product-info py-20 lg:py-32">
      <h3 class="text-center mb-8 lg:mb-14">机械情报</h3>
      <div class="container mx-auto">
        <div class="mx-auto max-w-[1200px] h-[415px] bg-[#d9d9d9]"></div>
      </div>
    </section>
    <section class="question w-screen bg-[#d9d9d9] py-20 lg:py-32">
      <div class="container mx-auto">
        <h3 class="text-black text-center mb-8 lg:mb-14">常见问题</h3>
        <div class="flex flex-col gap-8 lg:gap-12">
          <ClickDisplayList before-con="Q">
            questionquestion
            <template slot="content-video"></template>
            <template slot="content-detail"
              >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
            >
          </ClickDisplayList>
          <ClickDisplayList before-con="Q">
            questionquestion
            <template slot="content-video"></template>
            <template slot="content-detail"
              >描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述</template
            >
          </ClickDisplayList>
        </div>
      </div>
    </section>
    <section class="buy-consult w-screen bg-[#f7f7f7] py-20 lg:py-32">
      <div class="container mx-auto px-6 lg:px-0">
        <div class="flex flex-col lg:flex-row justify-evenly">
          <div>
            <h3 class="text-black mb-8 lg:mb-12">购买渠道</h3>
          </div>
          <div>
            <h3 class="text-black mb-8 lg:mb-12">技术咨询</h3>
          </div>
        </div>
      </div>
    </section>
    <section class="product-footer w-screen py-12 px-6 lg:px-0 lg:py-32">
      <div class="container mx-auto">
        <div class="grid grid-rows-2 lg:grid-cols-2 lg:max-h-[320px]">
          <div
            class="mx-auto w-[224px] flex flex-col justify-center items-center gap-10"
          >
            <Logo class="transform scale-[1.3]" show-text="false"></Logo>
            <Logo class="transform scale-[1.3]" show-logo="false"></Logo>
          </div>
          <div class="">
            <h3 class="mb-8 lg:mb-12">我们是？</h3>
            <p class="text-detail max-w-[738px] mb-10 lg:mb-14">
              文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文文本文本文本文本文本文本文本
            </p>
            <div class="w-full">
              <MoreBtn bg-class="text-black bg-white self-center mx-auto" />
            </div>
          </div>
        </div>
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
