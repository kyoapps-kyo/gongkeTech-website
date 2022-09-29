<template>
  <footer class="absolute bottom-0 left-0 h-[300px] lg:h-[326px] w-screen">
    <div
      class="container mx-auto pt-[20px] pb-[20px] lg:pt-[61px] lg:pb-[40px]"
    >
      <Logo
        class="mb-[22px] w-[120px] lg:w-[240px] mx-auto lg:mx-0 lg:mb-[44px]"
      />
      <div class="footer-info lg:overflow-hidden mb-[31px] lg:mb-[62px]">
        <div class="info-l lg:float-left">
          <Address
            class="mb-[12px] lg:mb-[12px] text-center lg:text-left w-[240px] lg:w-[460px] mx-auto lg:mx-0"
          />
          <Email class="text-center lg:text-left" />
        </div>
        <div
          class="info-r lg:float-right mx-auto lg:mx-0 w-[265px] mt-4 lg:mt-0"
        >
          <social-list></social-list>
        </div>
      </div>
      <Copyright />
    </div>
  </footer>
</template>
