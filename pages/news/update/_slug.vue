<template>
  <article class="bg-white px-6 lg:px-0 pb-20">
    <div class="prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto pt-4">
      <span
        class="cursor-pointer underline leading-[2.0]"
        @click="$router.back()"
        >返回上一页</span
      >
    </div>

    <div
      class="content-header prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto pt-16 lg:pt-20"
    >
      <span>{{ article.date }}</span>
      <h1>
        {{ article.title }}
      </h1>
    </div>
    <div class="max-w-[700px] min-w-[300px] mx-auto my-8 lg:my-8">
      <nuxt-img class="mx-auto" :src="article.img" sizes="xs:300 xxl:700" />
    </div>
    <nuxt-content
      class="prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto"
      :document="article"
    >
    </nuxt-content>
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('articles/update', params.slug).fetch()
    return { article }
  },
  head() {
    return {
      title: this.article.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.article.description,
        },
      ],
    }
  },
}
</script>
