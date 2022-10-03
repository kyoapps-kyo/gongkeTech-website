<template>
  <div>
    <div class="lg:flex text-center lg:text-left">
      <div class="mb-6 lg:mb-0 text-left">
        <ul class="flex lg:flex-col gap-4 lg:gap-10 lg:w-[350px]">
          <li
            v-for="(option, index) in selectList"
            :key="option"
            class="transition-all duration-500 cursor-pointer hover:scale-105 opacity-80"
            :class="selectIndex === index ? 'active' : ''"
            @click.stop="displayContent(index)"
          >
            {{ option }}
          </li>
        </ul>
      </div>
      <div class="grow py-8 lg:py-0">
        <h4 class="text-black mb-6 lg:mb-20">{{ selectList[selectIndex] }}</h4>
        <div class="max-w-[600px] h-[400px] bg-black mb-6 lg:mb-20"></div>
        <h5 class="text-black mb-6 lg:mb-14">
          {{ displayData.title }}
        </h5>
        <p class="text-detail max-w-[750px]" style="color: black">
          {{ displayData.content }}
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const data = ref<Object>([
  {
    type: 'pic',
    title: '标题1',
    content: '说明文本说明文本说明文本说明文本说明文本',
    src: '',
  },
  {
    type: 'pic',
    title: '标题2',
    content: '说明文本说明文本说明文本说明文本说明文本',
    src: '',
  },
  {
    type: 'pic',
    title: '标题3',
    content: '说明文本说明文本说明文本说明文本说明文本',
    src: '',
  },
  {
    type: 'pic',
    title: '标题4',
    content: '说明文本说明文本说明文本说明文本说明文本',
    src: '',
  },
  {
    type: 'pic',
    title: '标题5',
    content: '说明文本说明文本说明文本说明文本说明文本',
    src: '',
  },
])
const selectList = ['特点一', '特点二', '特点三', '特点四', '特点五']

const displayData = ref<Object>(data.value[0])
const selectIndex = ref<Number>(0)

const getData = (index) => {
  if (index) return data.value[index]
  return data.value[0]
}

const displayContent = (index: Number) => {
  if (!index) index = 0
  displayData.value = getData(index)
  selectIndex.value = index
}
</script>

<style scoped>
.active {
  font-weight: bold;
  font-size: 18px;
}
</style>
