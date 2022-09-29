<template>
  <ul class="look-down">
    <a href="#display-cards">
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
</template>
<style scoped>
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
