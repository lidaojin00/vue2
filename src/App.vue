<template>
  <div id="app">
    <my-header @clickHome="goHome"  @clickAbout="goAbout"/>
    <router-view/>
    <my-footer/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyFooter from './components/MyFooter.vue'

export default {
  name: 'app',
  components: {
    MyHeader,
    MyFooter
  },
  methods:{
    goHome:function(){
      this.$router.push("/");
    },
    goAbout:function(){
      this.$router.push("/about");
    }
  }
}
</script>

<style>
#app {
  height: 100vh;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
