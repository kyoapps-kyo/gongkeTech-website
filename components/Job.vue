<template>
  <div class="job-card w-screen py-8 lg:py-20">
    <h3 class="drop-shadow-[1px_1px_2px_#000] text-center mb-8 lg:mb-20">
      {{ jobs[ant][index].job }}
    </h3>
    <div
      class="container mx-auto px-6 lg:px-20 grid grid-cols-3 gap-y-6 gap-x-10 lg:gap-16 drop-shadow-[2px_2px_3px_#000] mb-8 lg:mb-20"
    >
      <div class="col-span-1">
        <h4 class="text-center">
          {{ jobKey[1] }}
        </h4>
      </div>
      <div class="col-span-2">
        <ul class="flex flex-col gap-4 text-detail">
          <li
            v-for="(item, index) in jobs[ant][index].content"
            :key="item + index"
          >
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="col-span-1">
        <h4 class="text-center">
          {{ jobKey[2] }}
        </h4>
      </div>
      <div class="col-span-2">
        <ul class="flex flex-col gap-4 text-detail">
          <li
            v-for="(item, index) in jobs[ant][index].require"
            :key="item + index"
          >
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="col-span-1">
        <h4 class="text-center">
          {{ jobKey[3] }}
        </h4>
      </div>
      <div class="col-span-2">
        <ul class="flex flex-col gap-4 text-detail">
          {{
            jobs[ant][index].address
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

const jobs = ref<Object[]>([
  [
    {
      job: '算法工程师',
      content: [
        '以脑电信号为导向，负责噪声、伪迹干扰去除的相关工作',
        '配合各事业群，完成相关任务的特征提取工作。如睡眠各分期脑电特征、精神疾病脑电特征、注意力、疲劳的脑电特征等',
        '完成相关文档的撰写',
      ],
      require: [
        '通信工程、电子工程、计算机工程、生物医学工程、自动化、数学等相关专业，硕士学历及以上',
        '具备扎实的编程能力(MATLAB, Python)',
        '具备扎实的数字信号处理理论基础。理解FFT如何实现、数字滤波器如何构建等',
        '对非线性非平稳信号的处理方法有深入的理解，如小波变换、经验模态分解、希尔伯特黄变换等',
        '具备良好的沟通能力和团队协作能力',
      ],
      address: '北京海淀 全职',
    },
    {
      job: '机电工程师',
      content: [
        '以脑电信号为导向，负责噪声、伪迹干扰去除的相关工作',
        '配合各事业群，完成相关任务的特征提取工作。如睡眠各分期脑电特征、精神疾病脑电特征、注意力、疲劳的脑电特征等',
        '完成相关文档的撰写',
      ],
      require: [
        '通信工程、电子工程、计算机工程、生物医学工程、自动化、数学等相关专业，硕士学历及以上',
        '具备扎实的编程能力(MATLAB, Python)',
        '具备扎实的数字信号处理理论基础。理解FFT如何实现、数字滤波器如何构建等',
        '对非线性非平稳信号的处理方法有深入的理解，如小波变换、经验模态分解、希尔伯特黄变换等',
        '具备良好的沟通能力和团队协作能力',
      ],
      address: '北京海淀 全职',
    },
  ],
  [
    {
      job: '算法实习',
      content: [
        '以脑电信号为导向，负责噪声、伪迹干扰去除的相关工作',
        '配合各事业群，完成相关任务的特征提取工作。如睡眠各分期脑电特征、精神疾病脑电特征、注意力、疲劳的脑电特征等',
        '完成相关文档的撰写',
      ],
      require: [
        '通信工程、电子工程、计算机工程、生物医学工程、自动化、数学等相关专业，硕士学历及以上',
        '具备扎实的编程能力(MATLAB, Python)',
        '具备扎实的数字信号处理理论基础。理解FFT如何实现、数字滤波器如何构建等',
        '对非线性非平稳信号的处理方法有深入的理解，如小波变换、经验模态分解、希尔伯特黄变换等',
        '具备良好的沟通能力和团队协作能力',
      ],
      address: '北京海淀 全职',
    },
    {
      job: 'CV实习',
      content: [
        '以脑电信号为导向，负责噪声、伪迹干扰去除的相关工作',
        '配合各事业群，完成相关任务的特征提取工作。如睡眠各分期脑电特征、精神疾病脑电特征、注意力、疲劳的脑电特征等',
        '完成相关文档的撰写',
      ],
      require: [
        '通信工程、电子工程、计算机工程、生物医学工程、自动化、数学等相关专业，硕士学历及以上',
        '具备扎实的编程能力(MATLAB, Python)',
        '具备扎实的数字信号处理理论基础。理解FFT如何实现、数字滤波器如何构建等',
        '对非线性非平稳信号的处理方法有深入的理解，如小波变换、经验模态分解、希尔伯特黄变换等',
        '具备良好的沟通能力和团队协作能力',
      ],
      address: '北京海淀 全职',
    },
  ],
])
const jobKey = Object.keys(jobs.value[props.ant][props.index])
</script>

<style scoped>
.job-card {
  background: url(@/assets/images/job-card-bg.jpg) no-repeat center center /
    cover;
  background-attachment: fixed;
}
</style>
