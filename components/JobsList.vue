<template>
  <div>
    <h4 class="text-center mb-6 lg:mb-16">职位列表</h4>
    <ul
      class="lg:w-[834px] mx-auto w-full flex flex-col flex-wrap justify-start items-center lg:flex-row lg:justify-between lg:items-center gap-10 lg:gap-x-[234px] mb-8 lg:mb-20"
    >
      <li
        v-for="(item, index) in ant == 0 ? jobs.social : jobs.school"
        :key="item + index"
        class="w-[300px] h-[40px] border rounded-lg border-gray-300 text-detail text-center leading-[40px] cursor-pointer hover:text-black hover:bg-white hover:border-black"
        :class="num == index ? 'bg-gray-400' : ''"
        @click="active(index)"
      >
        {{ item }}
      </li>
    </ul>
    <div class="job-card">
      <Job v-show="num == jobIndex" :index="jobIndex" :ant="ant" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const props = defineProps({
  ant: { type: Number, default: 1 },
})

const num = ref<Number | null>(null)
const jobIndex = ref<Number>(0)

const jobs = ref({
  social: ['算法工程师', '电机工程师'],
  school: ['算法实习', '电机实习'],
})

const active = (index: number) => {
  jobIndex.value = index
  if (num.value !== index) {
    num.value = index
  } else num.value = null
  console.log(num.value)
}
</script>
