<template>
  <section class="banner w-full h-screen">
    <div class="container mx-auto relative h-screen">
      <div
        class="banner-con flex flex-col items-start h-full lg:h-fit lg:w-[920px] pt-24 px-8 lg:py-10 lg:px-10 bg-black/50 lg:bg-black/30 backdrop-blur-sm lg:absolute lg:top-1/2 lg:mt-[-320px] lg:rounded-lg"
      >
        <div class="slogan mb-8 lg:mb-[82px]">
          <nuxt-img src="logo-slogan-w.png" sizes="md:200px xxl:400px" />
        </div>
        <div
          class="banner-description text-[18px] lg:text-[24px] text-white leading-loose"
        >
          Lorem Ipsum，也称乱数假文或者哑元文本，
          是印刷及排版领域所常用的虚拟文字。由于曾经一台匿名的打印机刻意打乱了一盒印刷字体从而造出一本字体样品书，Lorem
          Ipsum从西元15世纪起就被作为此领域的标准文本使用。
        </div>
        <a
          class="text-white block text-center cursor-pointer self-center mt-8 lg:self-auto lg:absolute lg:top-1/2 lg:-right-[24rem] lg:mt-[-150px] transition-all transform hover:scale-[1.2] hover:text-[#e5e5e5]"
        >
          <span class="iconfont text-[60px] lg:text-[160px]">&#xe606;</span>
          <br />
          <span class="text-[16px] lg:text-[22px]">观看完整介绍</span>
        </a>
      </div>
      <ul
        class="look-down absolute bottom-[30%] text-white left-1/2 text-[40px] ml-[-20px] lg:text-[80px] lg:ml-[-40px]"
      >
        <a href="">
          <li>
            <span class="iconfont absolute top-0">&#xe626;</span>
          </li>
          <li>
            <span class="iconfont absolute top-4">&#xe626;</span>
          </li>
          <li>
            <span class="iconfont absolute top-8">&#xe626;</span>
          </li>
        </a>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.banner {
  background: #000 url('@/assets/images/banner-bg.jpg') no-repeat center center /
    auto 100%;
  background-blend-mode: hard-light;
  filter: saturate(30%);
  background-attachment: fixed;
}
.look-down li span.iconfont {
  scale: 0.2;
  opacity: 0;
  translate: 0px 0px;
  animation-name: look-down;
  animation-timing-function: leaner;
  animation-iteration-count: infinite;
}
.look-down li:nth-of-type(1) span.iconfont {
  animation-delay: 400ms;
  animation-duration: 2000ms;
}
.look-down li:nth-of-type(2) span.iconfont {
  animation-delay: 200ms;
  animation-duration: 2000ms;
}
.look-down li:nth-of-type(3) span.iconfont {
  animation-duration: 2000ms;
}

@keyframes look-down {
  0% {
    scale: 0.2;
    opacity: 0;
    translate: 0px 0px;
  }

  80% {
    scale: 1.2;
    opacity: 1;
    translate: 0px 80px;
  }

  100% {
    scale: 0.2;
    opacity: 0;
    translate: 0px 100px;
  }
}
</style>
