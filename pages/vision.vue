<template>
  <div>
    <OtherBanner>
      <template slot="subtitle"> {{ $t('pages.vision.subtitle') }} </template>
      <template slot="title"> {{ $t('pages.vision.title') }} </template>
      <template slot="description">
        {{ $t('pages.vision.description') }}
      </template>
    </OtherBanner>
    <VisionCon />
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: '公司愿景',
    }
  },
}
</script>
