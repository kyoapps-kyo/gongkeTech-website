# gongkeTech-website-nuxt2

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## 网页内容修改位置

```bash
# 文字内容修改
# 三个文件依次对应中日英文

/locales
    |---------------/ zh.json
    |---------------/ ja.json
    |---------------/ en.json

# 图片存放位置
# 在nuxt-img中使用图片，只需要输入文件名+后缀，例如：avatar.jpg

/assets
    |---------------/ images


# 新文章存放位置
# 文章格式参照nuxt/content,图片直接使用文件名+后缀
/content
    |----/ articles
        |----/ release
        |----/ update

```
