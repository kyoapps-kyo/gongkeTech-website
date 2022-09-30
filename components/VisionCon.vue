<template>
  <section class="vision-con">
    <div
      class="pt-[20px] lg:pt-[40px] container mx-auto px-4 lg:px-0 text-white"
    >
      <VisionConTextDisplay class="pb-[40px] lg:pb-[80px]">
        <span class="text-description leading-[40px] lg:leading-[60px]">
          它使用由超过200个拉丁单词所构造的词典，<br />
          结合了几个模范句子结构，来生成看起来恰当的Lorem Ipsum。<br />
          因此，生成出的结果无一例外免于重复，刻意的幽默，以及非典型的词汇等等。<br />
          结合了几个模范句子结构，来生成看起来恰当的Lorem Ipsum。<br />
          它使用由超过200个拉丁单词所构造的词
        </span>
      </VisionConTextDisplay>
      <VisionConTextDisplay class="pb-[40px] lg:pb-[80px]">
        <template slot="title">什么是Lorem Ipsum?</template>
        <template slot="content"
          >无可否认，当读者在浏览一个页面的排版时，难免会被可阅读的内容所分散注意力。Lorem
          Ipsum的目的就是为了保持字母多多少少标准及平均的分配，而不是“此处有文本，此处有文本”，从而让内容更像可读的英语。如今，很多桌面排版软件以及网页编辑用Lorem
          Ipsum作为默认的示范文本，搜一搜“Lorem
          Ipsum”就能找到这些网站的雏形。这些年来Lorem
          Ipsum演变出了各式各样的版本，有些出于偶然，有些则是故意的（刻意的幽默之类的）。</template
        >
      </VisionConTextDisplay>
      <VisionConTextDisplay class="pb-[40px] lg:pb-[80px]">
        <template slot="title">什么是Lorem Ipsum?</template>
        <template slot="content"
          >无可否认，当读者在浏览一个页面的排版时，难免会被可阅读的内容所分散注意力。Lorem
          Ipsum的目的就是为了保持字母多多少少标准及平均的分配，而不是“此处有文本，此处有文本”，从而让内容更像可读的英语。如今，很多桌面排版软件以及网页编辑用Lorem
          Ipsum作为默认的示范文本，搜一搜“Lorem
          Ipsum”就能找到这些网站的雏形。这些年来Lorem
          Ipsum演变出了各式各样的版本，有些出于偶然，有些则是故意的（刻意的幽默之类的）。</template
        >
      </VisionConTextDisplay>
      <VisionConTextDisplay class="pb-[40px] lg:pb-[80px]">
        <template slot="title">什么是Lorem Ipsum?</template>
        <template slot="content"
          >无可否认，当读者在浏览一个页面的排版时，难免会被可阅读的内容所分散注意力。Lorem
          Ipsum的目的就是为了保持字母多多少少标准及平均的分配，而不是“此处有文本，此处有文本”，从而让内容更像可读的英语。如今，很多桌面排版软件以及网页编辑用Lorem
          Ipsum作为默认的示范文本，搜一搜“Lorem
          Ipsum”就能找到这些网站的雏形。这些年来Lorem
          Ipsum演变出了各式各样的版本，有些出于偶然，有些则是故意的（刻意的幽默之类的）。</template
        >
      </VisionConTextDisplay>
    </div>
    <div
      class="container mx-auto transition-all duration-500 opacity-60 translate-y-10 hover:opacity-100 hover:translate-y-0"
    >
      <div
        class="future w-full h-full px-4 lg:px-0 lg:w-[845px] lg:h-[845px] mx-auto text-white text-center pt-[20px] lg:pt-[71px] pb-[60px] lg:pb-[40px] mb-[100px] lg:mb-0"
      >
        <h4>未来进化历程</h4>
        <h6 class="mb-[50px] lg:mb-[100px] font-normal">
          FUTURE HISTORY of EVOLUTION
        </h6>
        <p class="text-detail lg:w-[600px] lg:mx-auto lg:mb-[120px] mb-[60px]">
          文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述文字描述
        </p>
        <div class="w-full">
          <MoreBtn bg-class="bg-white text-black mx-auto" />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup></script>

<style scoped>
.future {
  background: #000 url(@/assets/images/future-bg.jpg) no-repeat center center /
    cover;
  background-blend-mode: hard-light;
  filter: saturate(90%);
}
</style>
