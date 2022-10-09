<template>
  <div
    class="h-[400px] w-[600px] mx-auto flex flex-col justify-center items-center text-white text-center"
  >
    <h2>{{ $t('welcome') }}</h2>
    <h2>{{ $t('pages.index.title') }}</h2>
    <h2>{{ $t('pages.index.data.0') }}</h2>
    <nuxt-link :to="switchLocalePath('zh')">中文</nuxt-link>
    <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
    <nuxt-link :to="switchLocalePath('ja')">japanese</nuxt-link>
  </div>
</template>
