<template>
  <div>
    <dl class="cursor-pointer language relative">
      <dt @click="modal = true">{{ getLangName($i18n.locale) }}</dt>
      <dd
        v-if="modal"
        v-on-click-outside="langSwitch"
        class="absolute top-[50px] left-[-80px] w-[250px] h-[48px] lg:w-[200px] lg:top-[4px] lg:left-[-200px] rounded-xl backdrop-blur-sm bg-white/40"
      >
        <ul class="flex justify-evenly items-center m-auto h-[48px]">
          <li><nuxt-link :to="switchLocalePath('zh')">中文</nuxt-link></li>
          <li><nuxt-link :to="switchLocalePath('en')">English</nuxt-link></li>
          <li><nuxt-link :to="switchLocalePath('ja')">日本語</nuxt-link></li>
        </ul>
      </dd>
    </dl>
    <span class="iconfont text-[20px] cursor-pointer" @click="modal = true"
      >&#xe61a;</span
    >
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import { vOnClickOutside } from '@vueuse/components'

const modal = ref(false)

function langSwitch() {
  modal.value = false
}
function getLangName(lang: string) {
  switch (lang) {
    case 'zh':
      return '中文'
    case 'en':
      return 'English'
    case 'ja':
      return '日本語'
  }
}
</script>

<style scoped>
.language {
  display: inline-block;
  color: white;
  position: relative;
}

dd {
  z-index: 999;
  box-sizing: border-box;
}
</style>
