<template>
  <div class="index-page-content">
    <IndexPageBanner />
    <section id="display-cards" class="display-cards w-screen">
      <div class="container mx-auto lg:grid lg:grid-cols-2">
        <div
          class="product-card col-span-2 h-[490px] w-full box-border px-[16px] pt-[120px] pb-[40px] lg:px-[138px] lg:pt-[101px] lg:pb-[70px] flex flex-col justify-start tracking-wide"
        >
          <h2 class="mb-2 lg:mb-6 text-black">产品名称</h2>
          <p
            class="text-description font-bold lg:w-[620px] mb-8"
            style="color: #000"
          >
            产品简述产品简述产品简述产品简述产品简述产品简述
          </p>
          <p
            class="grow text-detail lg:w-[620px] leading-[2.0]"
            style="color: #000"
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
      <h4
        class="pt-[80px] mb-[20px] lg:mb-[80px] lg:pt-[120px] text-center w-full"
      >
        产品信息
      </h4>
      <div id="product-display-zoom">
        <ProductInfo
          v-for="(item, index) in $t('pages.index.productInfo')"
          :key="item.name + index"
          class="sticky top-0 product-info"
          :link="item.link"
          :no-bg-color="index == 0 ? false : true"
        >
          <template slot="subtitle">{{ item.name }}</template>
          <template slot="title">{{ item.title }}</template>
          <template slot="description">{{ item.description }}</template>
          <template slot="product-img">
            <nuxt-img :src="item.src" sizes="sm:390 xxl:506" />
          </template>
        </ProductInfo>
        <div
          class="sticky top-0 product-info h-[300px] lg:h-[500px] w-full"
        ></div>
      </div>
    </section>
    <section id="news">
      <NewsLists link="news" color="text-black" />
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
