<template>
  <div>
    <div class="lg:flex text-center lg:text-left">
      <div class="mb-6 lg:mb-0 text-left">
        <ul class="flex lg:flex-col gap-4 lg:gap-10 lg:w-[350px]">
          <li
            v-for="(item, index) in $t('pages.tech.tips.selectList')"
            :key="item + index"
            class="transition-all duration-500 cursor-pointer hover:scale-105 opacity-80"
            :class="selectIndex === index ? 'active' : ''"
            @click.stop="displayContent(index)"
          >
            {{ item }}
          </li>
        </ul>
      </div>
      <span class="hidden">{{ (data = $t('pages.tech.tips.items')) }}</span>
      <div class="grow py-8 lg:py-0">
        <h4 class="text-black mb-6 lg:mb-20">
          {{ $t('pages.tech.tips.selectList')[selectIndex] }}
        </h4>
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
import { ref, onMounted } from 'vue'

const data = ref<Object | null>(null)

const displayData = ref<Object>({ title: '', content: '' })
const selectIndex = ref<Number>(0)

const getData = (index: Number) => {
  if (index) return data.value[index]
  return data.value[0]
}

const displayContent = (index: Number) => {
  if (!index) index = 0
  displayData.value = getData(index)
  selectIndex.value = index
}

onMounted(() => {
  displayData.value = data.value[0]
})
</script>

<style scoped>
.active {
  font-weight: bold;
  font-size: 18px;
}
</style>
