<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        vant-ui-demo
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <Rate v-model="value"></Rate>
      <!-- <van-button>按钮</van-button> -->
      <Button>BB</Button>
      <!-- <Badge :count="1"> -->
      <!-- <Avatar shape="square" icon="user" /> -->
      <!-- </Badge> -->
    </div>
  </div>
</template>

<script>
import { Button } from 'vant'
// import { Rate, Badge, Avatar } from 'ant-design-vue'
import { Rate } from 'ant-design-vue'
// import '~node_modules/vant/lib/button/style'
// import '@/node_modules/ant-design-vue/lib/rate/style/index.css'
// import 'vant/lib/button/style/index.js'

export default {
  components: { Button, Rate },
  data() {
    return {
      value: 4,
    }
  },
}
</script>

<style lang="less" scoped>
.container {
  background-color: #ff0;
}
</style>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
  padding-bottom: 15px;
}
</style>
