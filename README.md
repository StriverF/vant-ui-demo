# vant-ui-demo

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

## 按需引入Vant / Ant Design Vue 组件库(样式也按需引入)
需要注意的是 Nuxt的`nuxt.config.js`配置里面的 [plugins](https://nuxtjs.org/guide/plugins) 第三方库引入配置是全局引入，不是按页面按需引入。
包括`nuxt.config.js`[css](https://zh.nuxtjs.org/api/configuration-css/)也是一样全局引入。

为了按需引入样式和组件需要配置`nuxt.config.js`的 [build]{https://zh.nuxtjs.org/api/configuration-build/}配置项
```javascript
export default {
  build: {
    babel: {
      plugins: [
        [
          'import',
          {
            libraryName: 'vant',
            style: (name) => {
              return `${name}/index.css`
            },
          },
        ],
      ]
    }
  }
}
```


For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
