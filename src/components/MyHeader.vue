<template>
  <div class="header">
    <P>我是Header</P>
    <div class="tab">
      <div v-on:click="switchTab('/')">首页</div>
      <div v-on:click="switchTab('/about')">关于我们</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyHeader",
  methods: {
    switchTab: function(path) {
      this.$emit('switchPath', path);
    }
  }
};
</script>
<style scoped>
.header {
  width: calc(100% - 200px);
  height: 180px;
  padding: 0 100px;
  background-color: #0479dc;
  color: #ffffff;
  position: relative;
}
.tab {
  position: absolute;
  bottom: 0;
}
.tab div {
  display: inline-block;
  padding: 10px 20px;
  background-color: cyan;
  margin-right: 10px;
}
</style>
