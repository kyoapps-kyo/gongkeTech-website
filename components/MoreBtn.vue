<!--
  bg-class控制按钮的背景色和文字颜色
  link跳转链接
-->
<template>
  <nuxt-link
    :to="link"
    class="block lg:h-[40px] h-[30px] w-[120px] lg:w-[140px] rounded-full text-center text-[12px] lg:text-[14px] leading-[30px] lg:leading-[40px] transition-all transform hover:scale-105 hover:bg-gray-600 hover:text-gray-100"
    :class="bgClass"
  >
    <slot>{{ $t('other.btnText') }}</slot>
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
