<template>
  <div id="app">
    <my-header @switchPath="goHome" />
    <router-view />
    <my-footer />
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue";
import MyFooter from "./components/MyFooter.vue";

export default {
  name: "app",
  components: {
    MyHeader,
    MyFooter
  },
  created(){
    alert(process.env.VUE_APP_BASE_URL);
  },
  methods: {
    goHome: function(path) {
      this.$router.push(path);
    }
  }
};
</script>

<style>
#app {
  height: 100vh;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
