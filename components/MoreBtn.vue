<!--
  bg-class控制按钮的背景色和文字颜色
  link跳转链接
-->
<template>
  <nuxt-link
    :to="link"
    class="block h-[40px] w-[140px] rounded-full text-center text-[14px] leading-[40px] transition-all transform hover:scale-105 hover:bg-gray-600 hover:text-gray-100"
    :class="bgClass"
  >
    查看更多
  </nuxt-link>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    bgClass: {
      type: String,
      default: '',
    },
    link: {
      type: String,
      default: '/',
    },
  },
})
</script>
