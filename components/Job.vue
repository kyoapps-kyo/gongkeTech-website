<template>
  <div class="job-card w-screen py-8 lg:py-20">
    <h3 class="drop-shadow-[1px_1px_2px_#000] text-center mb-8 lg:mb-20">
      {{ $t('pages.contact.jobList.jobs')[ant][index].job }}
    </h3>
    <div
      class="container mx-auto px-6 lg:px-20 grid grid-cols-3 gap-y-6 gap-x-10 lg:gap-16 drop-shadow-[2px_2px_3px_#000] mb-8 lg:mb-20"
    >
      <div class="col-span-1">
        <h5 class="text-center">内容 / CONTENT</h5>
      </div>
      <div class="col-span-2">
        <ul class="flex flex-col gap-4 text-detail">
          <li
            v-for="(item, index) in $t('pages.contact.jobList.jobs')[ant][index]
              .content"
            :key="item + index"
          >
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="col-span-1">
        <h5 class="text-center">要求 / REQUIRE</h5>
      </div>
      <div class="col-span-2">
        <ul class="flex flex-col gap-4 text-detail">
          <li
            v-for="(item, index) in $t('pages.contact.jobList.jobs')[ant][index]
              .require"
            :key="item + index"
          >
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="col-span-1">
        <h5 class="text-center">地址・类型 / ADDRESS</h5>
      </div>
      <div class="col-span-2">
        <ul class="flex flex-col gap-4 text-detail">
          {{
            $t('pages.contact.jobList.jobs')[ant][index].address
          }}
        </ul>
      </div>
    </div>
    <div class="w-full">
      <MoreBtn bg-class="bg-white mx-auto shadow-xl">申请岗位</MoreBtn>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const props = defineProps({
  index: { type: Number, default: 0 },
  ant: { type: Number, default: 0 },
})
</script>

<style scoped>
.job-card {
  background: url(@/assets/images/job-card-bg.jpg) no-repeat center center /
    cover;
  background-attachment: fixed;
}
</style>
