<template>
  <div class="menu">
    <Menu class="pc-menu hidden lg:block w-[830px] h-[58px]" />
    <a
      class="lg:hidden h-[40px] w-[40px] mt-[4px] block relative"
      @click="isShow = !isShow"
    >
      <transition name="btn">
        <span
          v-if="isShow"
          key="open"
          class="iconfont text-[28px] text-white absolute top-0"
          >&#xe6a7;</span
        >
        <span
          v-else
          key="close"
          class="iconfont text-[28px] text-white absolute top-0"
          >&#xe62f;</span
        >
      </transition>
    </a>
    <transition name="menu">
      <div
        v-if="isShow"
        class="mask h-screen w-screen bg-black bg-opacity-80 absolute top-[48px] left-0 flex flex-col items-center"
      >
        <Slogan />
        <Menu
          class="mobile-menu text-white h-[400px] w-[106px] text-2xl leading-[55px] tracking-wides text-center"
        />
      </div>
    </transition>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      isShow: false,
    }
  },
}
</script>

<style scoped>
.btn-enter-active {
  transition: all 0.8s ease;
}
.btn-leave-active {
  transition: all 0.3s cubic-bezier(1, 0.5, 0.8, 1);
}
.btn-enter, .btn-leave-to
/* .btn-leave-active for below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}

.menu-enter-active {
  transition: all 0.8s ease;
}
.menu-leave-active {
  transition: all 0.3s cubic-bezier(1, 0.5, 0.8, 1);
}
.menu-enter, .menu-leave-to
/* .menu-leave-active for below version 2.1.8 */ {
  transform: translateY(10px);
  opacity: 0;
}
</style>
