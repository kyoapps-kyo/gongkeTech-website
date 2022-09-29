<template>
  <main>
    <ul class="px-[16px] lg:px-0">
      <h3 class="text-[22px] font-normal mb-[20px] lg:mb-[43px]">最新资讯</h3>
      <li
        v-for="article of articles"
        :key="article.slug"
        class="mb-[34px] pb-[10px] border-b lg:h-[200px] lg:overflow-hidden"
      >
        <p
          class="text-[14px] lg:text-[16px] text-[#111] mb-[14px] lg:mb-[18px]"
        >
          {{ article.date }}
        </p>
        <div class="flex justify-between items-center">
          <div
            class="w-[80px] h-[80px] rounded-full overflow-hidden flex-none mr-[23px]"
          >
            <nuxt-img :src="article.img" width="80" height="80"></nuxt-img>
          </div>
          <NuxtLink :to="`news/update/${article.slug}`">
            <div>
              <h3 class="text-[20px] font-bold underline mb-[4px] lg:mb-[10px]">
                {{ article.title }}
              </h3>
              <p class="text-[18px]">{{ article.description }}</p>
            </div>
          </NuxtLink>
        </div>
      </li>
    </ul>
  </main>
</template>

<script>
export default {
  data() {
    return {
      articles: [],
    }
  },
  async fetch() {
    this.articles = await this.$content('articles/update')
      .only(['title', 'description', 'slug', 'date', 'img'])
      .sortBy('date', 'desc')
      .limit(5)
      .fetch()
  },
}
</script>
