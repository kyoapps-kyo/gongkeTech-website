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
    <section class="jobs">
      <div class="container mx-auto px-6 lg:px-24 py-4 lg:py-10">
        <h3 class="mb-4 lg:mb-8">JOIN US</h3>
        <ul
          class="w-[246px] h-[24px] flex justify-between items-center mb-8 lg:mb-10"
        >
          <li
            class="text-white text-[20px] cursor-pointer px-2 py-1 rounded-lg hover:border border-gray-300"
            :class="ant == 0 ? 'text-white font-bold' : 'text-gray-300'"
            @click="active(0)"
          >
            社会招聘
          </li>
          <li
            class="text-white text-[20px] cursor-pointer px-2 py-1 rounded-lg hover:border border-gray-300"
            :class="ant == 1 ? 'text-white font-bold' : 'text-gray-300'"
            @click="active(1)"
          >
            校园招聘
          </li>
        </ul>
      </div>
      <div class="jobs-list">
        <JobsList :ant="ant" />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ant: 0,
    }
  },
  head() {
    return {
      title: '联系我们',
    }
  },
  methods: {
    active(num) {
      this.ant = num
    },
  },
}
</script>

<style scoped>
.contact-banner {
  background: url(@/assets/images/contact-bg.jpg) no-repeat center center /
    cover;
}
</style>
