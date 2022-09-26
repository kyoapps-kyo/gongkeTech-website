<template>
  <div class="index-page-content">
    <Banner />
    <div class="bg-green-400 h-screen"></div>
    <div class="bg-blue-400 h-screen"></div>
    <div class="bg-red-400 h-screen"></div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Banner from '~/components/Banner.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: { Banner },
})
</script>
