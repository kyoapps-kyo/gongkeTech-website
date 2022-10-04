<template>
  <ul>
    <li>
      <nuxt-link to="/vision" class="w-full h-full block">公司愿景</nuxt-link>
    </li>
    <li>
      <nuxt-link to="/product" class="w-full h-full block">产品信息</nuxt-link>
    </li>
    <li>
      <nuxt-link to="/tech" class="w-full h-full block">技术支持</nuxt-link>
    </li>
    <li>
      <nuxt-link to="/about" class="w-full h-full block">关于我们</nuxt-link>
    </li>
    <li>
      <nuxt-link to="/newspage" class="w-full h-full block">新闻资讯</nuxt-link>
    </li>
    <li>
      <nuxt-link to="#" class="w-full h-full block">联系我们</nuxt-link>
    </li>
    <li><language-switch></language-switch></li>
  </ul>
</template>

<style scoped>
.pc-menu {
  overflow: hidden;
  width: 830px;
  color: rgb(192, 192, 192);
}
.pc-menu > li {
  float: left;
  height: 58px;
  width: 90px;
  line-height: 58px;
  margin-left: 32px;
  text-align: right;
  transition: all 1s linear 0s;
  border-bottom: none;
}

.pc-menu > li:hover {
  border-bottom: 1px solid rgb(165, 201, 255);
  color: rgb(165, 201, 255);
}

.pc-menu > li:first-child {
  margin-left: 0px;
}

.mobile-menu {
  color: rgb(192, 192, 192);
}

.mobile-menu > li {
  border-bottom: solid 2px rgb(211, 211, 211);
}

.mobile-menu > li:last-child {
  border-bottom: none;
}
ul > li > a {
  text-align: center;
}

a.nuxt-link-active {
  font-weight: bold;
}

a.nuxt-link-exact-active {
  color: #ffffff;
}
</style>
