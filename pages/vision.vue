<template>
  <div>
    <OtherBanner>
      <template slot="subtitle"> 公司愿景 </template>
      <template slot="title"> Lorem Ipsum从西元15世 </template>
      <template slot="description">
        Lorem Ipsum，也称乱数假文或者哑元文本
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
