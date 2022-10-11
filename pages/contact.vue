<template>
  <div>
    <div
      class="contact-banner h-[490px] w-screen flex flex-col justify-center items-center"
    >
      <h2 class="drop-shadow-[1px_1px_2px_#000]">
        {{ $t('pages.contact.slogan') }}
      </h2>
    </div>
    <section class="access">
      <div
        class="container mx-auto px-6 lg:px-24 py-8 lg:py-24 lg:flex lg:justify-between items-center"
      >
        <div class="pr-0 lg:pr-16">
          <h3 class="mb-4 lg:mb-8">ACCESS</h3>
          <h4 class="mb-6 lg:mb-10">{{ $t('pages.contact.company') }}</h4>
          <p class="text-detail mb-6 lg:mb-0" style="color: white">
            {{ $t('pages.contact.address') }}
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
            {{ $t('pages.contact.social') }}
          </li>
          <li
            class="text-white text-[20px] cursor-pointer px-2 py-1 rounded-lg hover:border border-gray-300"
            :class="ant == 1 ? 'text-white font-bold' : 'text-gray-300'"
            @click="active(1)"
          >
            {{ $t('pages.contact.school') }}
          </li>
        </ul>
      </div>
      <div class="jobs-list">
        <JobsList :ant="ant" />
      </div>
    </section>
    <section class="contact-form">
      <div class="bg-[#f7f7f7] py-8 lg:py-24">
        <h4 class="text-black text-center">
          {{ $t('pages.contact.contact.title') }}
        </h4>

        <form action="#" method="post">
          <div
            class="px-6 lg:px-0 w-full lg:w-[662px] mx-auto flex flex-col items-center gap-y-4 lg:gap-y-8 pt-6 lg:pt-20"
          >
            <input
              class="bg-[#f7f7f7] w-full h-[40px] border-2 rounded-xl pl-4 lg:pl-10 focus:bg-black text-white"
              type="text"
              :placeholder="$t('pages.contact.contact.name')"
            />
            <input
              class="bg-[#f7f7f7] w-full h-[40px] border-2 rounded-xl pl-4 lg:pl-10 focus:bg-black text-white"
              type="text"
              :placeholder="$t('pages.contact.contact.email')"
            />
            <input
              class="bg-[#f7f7f7] w-full h-[40px] border-2 rounded-xl pl-4 lg:pl-10 focus:bg-black text-white"
              type="text"
              :placeholder="$t('pages.contact.contact.phone')"
            />
            <input
              class="bg-[#f7f7f7] w-full h-[40px] border-2 rounded-xl pl-4 lg:pl-10 focus:bg-black text-white"
              type="text"
              :placeholder="$t('pages.contact.contact.content')"
            />
            <MoreBtn bg-class="bg-black text-white">{{
              $t('pages.contact.contact.submit')
            }}</MoreBtn>
          </div>
        </form>
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
