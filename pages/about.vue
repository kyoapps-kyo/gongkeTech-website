<template>
  <div>
    <OtherBanner class="about-banner">
      <template slot="subtitle">关于我们</template>
      <template slot="title">团队理念团队理念团队理念团队</template>
      <template slot="description">简述简述简述简述简述简述简述简述</template>
    </OtherBanner>
    <section class="team w-screen bg-white">
      <div class="py-10 lg:py-20 container mx-auto px-6 lg:px-0">
        <h3 class="text-center text-black mb-8 lg:mb-20">团队成员</h3>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-y-6 mb-8 lg:mb-20">
          <TeamMember class="mx-auto">
            <template slot="avatar">
              <nuxt-img src="avatar.png" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">姓名</template>
            职责
          </TeamMember>
          <TeamMember class="mx-auto">
            <template slot="avatar">
              <nuxt-img src="avatar.png" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">姓名</template>
            职责
          </TeamMember>
          <TeamMember class="mx-auto">
            <template slot="avatar">
              <nuxt-img src="avatar.png" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">姓名</template>
            职责
          </TeamMember>
          <TeamMember class="mx-auto">
            <template slot="avatar">
              <nuxt-img src="avatar.png" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">姓名</template>
            职责
          </TeamMember>
          <TeamMember class="mx-auto">
            <template slot="avatar">
              <nuxt-img src="avatar.png" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">姓名</template>
            职责
          </TeamMember>
          <TeamMember class="mx-auto">
            <template slot="avatar">
              <nuxt-img src="avatar.png" sizes="sm:120 xxl:180"></nuxt-img>
            </template>
            <template slot="name">姓名</template>
            职责
          </TeamMember>
        </div>
        <p
          class="text-description mb-8 lg:mb-20 max-w-[890px] mx-auto"
          style="color: black"
        >
          团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念团队构建理念
        </p>
        <div class="w-full">
          <MoreBtn bg-class="bg-black text-white mx-auto">加入我们</MoreBtn>
        </div>
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
