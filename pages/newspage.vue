<template>
  <div>
    <NewsLists :limit="100" color="text-black" :show="false" />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '新闻资讯',
    }
  },
}
</script>
