<template>
  <div class="logo">
    <Nuxt-link to="/" class="text-white inline-block">
      <h1 class="hidden">攻壳智动,脑机接口</h1>
      <nuxt-picture
        v-if="showLogo == 'true'"
        src="logo-w.png"
        alt="攻壳智动LOGO"
        sizes="md:30px xxl:42px"
        :img-attrs="{ class: 'inline-block' }"
      />
      <nuxt-picture
        v-if="showText == 'true'"
        src="logo-slogan-w.png"
        alt="攻壳智动SLOGAN"
        sizes="md:70px xxl:96px"
        :img-attrs="{ class: getTextClass }"
      />
    </Nuxt-link>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Logo',

  props: {
    showLogo: {
      type: String,
      default: 'true',
    },
    showText: {
      type: String,
      default: 'true',
    },
  },
  computed: {
    getTextClass(): string {
      return this.$props.showLogo === 'false'
        ? 'block'
        : 'inline-block ml-2 lg:ml-4'
    },
  },
})
</script>
