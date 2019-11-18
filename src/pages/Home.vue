<template>
  <div class="home">
    <p>我是首页</p>
    <button @click="go1">我是去自己项目的页面</button>
    <button @click="go2">我是去别项目的页面</button>
  </div>
</template>

<script>
export default {
  methods: {
    go1: function() {
      this.$router.push({
        name: "about",
        query: {
          token: "iamtoken啦啦啦啦",
          userID:"我是userID",
          form:"自己",
        }
      });
    },
    go2: function() {
      let url = "http://127.0.0.1:886/H5/vue2/#/about";
      let queryStr = "?token=我是来自别&form=别人"
      window.location.href = url + queryStr;
      //这里并不能用this.$router，因为你的router里面并没有别的项目的路由信息
    }
  }
};
</script>

<style scoped>
.home {
  height: calc(100% - 330px);
  text-align: center;
}
.home p {
  font-size: 30px;
  font-weight: 600;
  color: darkorchid;
}
</style>
