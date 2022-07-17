<template>
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reverseMsg() }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello Computed!!!",
    };
  },
  computed: {
    reversedMsg() {
      return this.msg.split("").reverse().join("");
    }, // 계산된 데이터, 캐싱
  },
  methods: {
    reverseMsg() {
      return this.msg.split("").reverse().join("");
    },
  },
};
</script>

<style scoped>
h1 {
  font-size: 100px;
}
</style>
