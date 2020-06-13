<template>
  <div id="app">
    <h1>{{ ttl }}</h1>
    <img alt="Vue logo" src="./assets/cherry-chan.png" />
    <Talk msg2="古代兵装・兜" />
  </div>
</template>

<script>
import Talk from "./components/Talk.vue";

export default {
  data() {
    return {
      ttl: "ワシのかわいい　チェリーちゃん"
    };
  },
  components: {
    Talk
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
