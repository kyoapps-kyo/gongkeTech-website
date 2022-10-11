<template>
  <div class="w-[1100px] h-[420px] relative">
    <div
      class="absolute w-[60px] h-[60px] border-2 border-[#60a9ff] top-1/2 left-0 mt-[-30px] text-[#60a9ff] text-[60px] text-center leading-[50px] cursor-pointer transform hover:scale-110 transition-all duration-1000 hover:bg-white"
      @click="leftMove"
    >
      &lt;
    </div>
    <div
      class="absolute w-[60px] h-[60px] border-2 border-[#60a9ff] top-1/2 right-0 mt-[-30px] text-[#60a9ff] text-[60px] text-center leading-[50px] cursor-pointer transform hover:scale-110 transition-all duration-1000 hover:bg-white"
      @click="rightMove"
    >
      &gt;
    </div>
    <div class="process-bar mx-auto"></div>
    <div
      ref="el"
      class="overflow-x-scroll absolute w-[700px] h-[340px] top-1/2 left-1/2 mt-[-170px] ml-[-350px] scroll-box"
    >
      <ul class="overflow-hidden h-[340px] w-max">
        <li
          v-for="(item, index) in $t('pages.about.history.items')"
          :key="item.index"
          class="h-[340px] w-[200px] relative"
        >
          <span v-if="index % 2 == 0" class="point-line-up"></span>
          <span v-else class="point-line-down"></span>
          <div
            v-if="index % 2 == 0"
            class="absolute top-1/4 transform translate-y-[-50%] left-[45px]"
          >
            <p class="text-[#60a9ff]">{{ item.date }}</p>
            <h5 class="text-black w-[200px] break-all">{{ item.title }}</h5>
          </div>
          <div
            v-else
            class="absolute bottom-1/4 transform translate-y-[50%] left-[45px]"
          >
            <p class="text-[#60a9ff]">{{ item.date }}</p>
            <h5 class="text-black w-[200px] break-all">{{ item.title }}</h5>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import { useScroll } from '@vueuse/core'

const el = ref<HTMLElement | null>(null)
const { x, arrivedState } = useScroll(el, {
  behavior: 'smooth',
})
const rightMove = () => {
  if (!arrivedState.right) x.value += 250
}
const leftMove = () => {
  if (!arrivedState.left) x.value -= 250
}
</script>

<style scoped>
.point-line-up {
  position: relative;
  display: inline-block;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  background-color: #60a9ff;
}
.point-line-up::before {
  content: '';
  position: absolute;
  width: 6px;
  height: 110px;
  background-color: #60a9ff;
  top: 30px;
  left: 12px;
}

.point-line-down {
  position: relative;
  display: inline-block;
  width: 6px;
  height: 110px;
  background-color: #60a9ff;
  top: 200px;
}
.point-line-down::before {
  content: '';
  border-radius: 50%;
  width: 30px;
  height: 30px;
  position: absolute;
  background-color: #60a9ff;
  top: 100px;
  left: -12px;
}
.process-bar {
  width: 1000px;
  height: 20px;
  position: absolute;
  top: 50%;
  margin-top: -10px;
  left: 50%;
  margin-left: -500px;
  background-image: linear-gradient(
    90deg,
    transparent 10%,
    #60a9ff,
    transparent 90%
  );
}

ul > li {
  float: left;
}

.scroll-box::-webkit-scrollbar {
  display: none;
}
.scroll-box {
  scrollbar-width: none; /* firefox */
  -ms-overflow-style: none; /* IE 10+ */
}
</style>
