<template>
  <div>
    <OtherBanner class="about-banner">
      <template slot="subtitle">{{
        $t('pages.about.banner.subtitle')
      }}</template>
      <template slot="title">{{ $t('pages.about.banner.title') }}</template>
      <template slot="description">{{
        $t('pages.about.banner.description')
      }}</template>
    </OtherBanner>
    <section class="team w-screen bg-white">
      <div class="py-10 lg:py-20 container mx-auto px-6 lg:px-0">
        <h3 class="text-center text-black mb-8 lg:mb-20">团队成员</h3>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-y-6 mb-8 lg:mb-20">
          <TeamMember
            v-for="(item, index) in $t('pages.about.teams.items')"
            :key="item + index"
            class="mx-auto"
          >
            <template slot="avatar">
              <nuxt-img :src="item.avatar" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">{{ item.name }}</template>
            {{ item.work }}
          </TeamMember>
        </div>
        <p
          class="text-description mb-8 lg:mb-20 max-w-[890px] mx-auto"
          style="color: black"
        >
          {{ $t('pages.about.constructor') }}
        </p>
        <div class="w-full">
          <MoreBtn bg-class="bg-black text-white mx-auto">{{
            $t('pages.about.join')
          }}</MoreBtn>
        </div>
      </div>
    </section>
    <section
      class="hidden lg:block history w-screen bg-[#f7f7f7f7] py-10 lg:py-20"
    >
      <h3 class="text-center text-black mb-6 lg:mb-14">
        {{ $t('pages.about.history.title') }}
      </h3>
      <h5 class="text-center text-black mb-10 lg:mb-20">
        {{ $t('pages.about.history.subtitle') }}
      </h5>
      <div
        class="container mx-auto px-6 lg:px-24 flex justify-center items-center"
      >
        <History />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '关于我们',
    }
  },
}
</script>
