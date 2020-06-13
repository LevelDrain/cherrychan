<template>
  <p>{{ msg[0] + msg2 + msg[1] }}</p>
</template>

<script>
export default {
  data() {
    return {
      msg: ["マイド ", " ニ変換スルンヤナ ワレ"] //App.vue へ出力
    };
  },
  props: {
    msg2: String //App.vue からの入力
  }
};
</script>

<style></style>
