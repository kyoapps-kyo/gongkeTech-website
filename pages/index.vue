<template>
  <div class="index-page-content">
    <Banner />
    <section id="display-cards" class="display-cards w-screen">
      <div class="container mx-auto lg:grid lg:grid-cols-2">
        <div
          class="product-card col-span-2 h-[490px] w-full box-border px-[16px] pt-[120px] pb-[40px] lg:px-[138px] lg:pt-[101px] lg:pb-[70px] flex flex-col justify-start tracking-wide"
        >
          <h2 class="text-[36px] lg:text-[56px] font-bold mb-2 lg:mb-6">
            产品名称
          </h2>
          <p class="text-[18px] lg:text-[24px] font-bold lg:w-[620px] mb-8">
            产品简述产品简述产品简述产品简述产品简述产品简述
          </p>
          <p
            class="grow text-[16px] lg:text-[16px] font-bold lg:w-[620px] leading-[2.0]"
          >
            详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述详细描述
          </p>
          <MoreBtn class="self-center" bg-class="bg-black text-white" />
        </div>
        <div class="h-[490px] w-full box-border">
          <CardCon class="vision-card">
            <template slot="subtitle">公司愿景</template>
            <template slot="title">标题标题标题标题</template>
            <template slot="description">描述描述描述描述描述</template>
          </CardCon>
        </div>
        <div class="h-[490px] w-full box-border">
          <CardCon class="tech-card">
            <template slot="subtitle">技术支持</template>
            <template slot="title">标题标题标题标题</template>
            <template slot="description">描述描述描述描述描述</template>
          </CardCon>
        </div>
      </div>
    </section>
    <section id="display-products" class="w-screen">
      <h2
        class="pt-[80px] mb-[20px] lg:mb-[80px] lg:pt-[120px] text-center w-full text-white text-[24px] font-bold"
      >
        产品信息
      </h2>
      <div id="product-display-zoom">
        <ProductInfo
          class="sticky top-0 product-info"
          link="product"
          :no-bg-color="false"
        >
          <template slot="subtitle">系列名称</template>
          <template slot="title">名称名称名称名称</template>
          <template slot="description">
            描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述
          </template>
          <template slot="product-img">
            <nuxt-img src="product-img1.png" sizes="sm:390 xxl:506" />
          </template>
        </ProductInfo>
        <ProductInfo class="sticky top-0 product-info" link="product">
          <template slot="subtitle">系列名称</template>
          <template slot="title">名称名称名称名称</template>
          <template slot="description">
            描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述
          </template>
          <template slot="product-img">
            <nuxt-img src="product-img2.png" sizes="sm:390 xxl:506" />
          </template>
        </ProductInfo>
        <ProductInfo class="sticky top-0 product-info" link="product">
          <template slot="subtitle">系列名称</template>
          <template slot="title">名称名称名称名称</template>
          <template slot="description">
            描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述
          </template>
          <template slot="product-img">
            <nuxt-img src="product-img3.png" sizes="sm:390 xxl:506" />
          </template>
        </ProductInfo>
        <div
          class="sticky top-0 product-info h-[300px] lg:h-[500px] w-full"
        ></div>
      </div>
    </section>
    <section id="news">
      <NewsLists />
    </section>
  </div>
</template>

<script lang="ts">
export default {
  head() {
    return {
      title: '首页',
    }
  },
}
</script>
<style scoped>
.product-card {
  background: url(@/assets/images/product-card-bg.jpg) no-repeat center center /
    cover;
}
</style>
