<template>
  <div class="footer">
    <P>我是Footer</P>
    <P class="dic">
      Cipyright @ 版权所有：四川省卫生健康委员会 管理单位：四川省卫生健康政策和医学情报研究所
      <br />瞎写瞎写瞎瞎写
      <br />软件开发、维护单位：我一点也不关心
    </P>
  </div>
</template>

<script>
export default {
  name: "MyFooter"
};
</script>

<style scoped>
.footer {
  width: 100%;
  height: 150px;
  background-color: #0479dc;
  color: #ffffff;
  text-align: center;
}
.dic {
  margin-top: 20px;
  line-height: 1.5em;
}
</style>
