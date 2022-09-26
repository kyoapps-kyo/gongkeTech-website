<template>
  <article class="pt-20">
    <nuxt-content :document="article" />
    <pre> {{ article }} </pre>
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    return { article }
  },
}
</script>
