<template>
  <article class="pt-20">
    <nuxt-content :document="article" />
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('articles/release', params.slug).fetch()
    console.log(params)
    return { article }
  },
}
</script>
