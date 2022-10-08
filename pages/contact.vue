<template>
  <div>
    <div
      class="contact-banner h-[490px] w-screen flex flex-col justify-center items-center"
    >
      <h2 class="drop-shadow-[1px_1px_2px_#000]">加入我们，共创未来</h2>
    </div>
    <section class="access">
      <div
        class="container mx-auto px-6 lg:px-24 py-8 lg:py-24 lg:flex lg:justify-between items-center"
      >
        <div class="pr-0 lg:pr-16">
          <h3 class="mb-4 lg:mb-8">ACCESS</h3>
          <h4 class="mb-6 lg:mb-10">攻壳智动</h4>
          <p class="text-detail mb-6 lg:mb-0" style="color: white">
            地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址地址
          </p>
        </div>
        <div class="h-[272px] w-full lg:w-[540px] bg-white"></div>
      </div>
    </section>
    <section class="jobs"></section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '联系我们',
    }
  },
}
</script>

<style scoped>
.contact-banner {
  background: url(@/assets/images/contact-bg.jpg) no-repeat center center /
    cover;
}
</style>
