<template>
  <div id="app">
    <h1>{{ ttl }}</h1>
    <img alt="Vue logo" src="./assets/cherry-chan.png" />
    <Talk msg2="古代兵装・兜" />
    <ShopList />
  </div>
</template>

<script>
import Talk from "./components/Talk.vue";
import ShopList from "./components/ShopList.vue";

export default {
  data() {
    return {
      ttl: "ワシのかわいい　チェリーちゃん"
    };
  },
  components: {
    Talk,
    ShopList
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
