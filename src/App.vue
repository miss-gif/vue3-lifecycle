<template>
  <button @click="add">add</button>
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
</template>

<script>
export default {
  data() {
    return {
      // Getter, Setter
      msg: "Hello Computed!!!",
    };
  },
  computed: {
    // Getter, 값을 얻어내는 용도
    // reversedMsg() {
    //   return this.msg.split("").reverse().join("");
    // }, // 계산된 데이터, 캐싱, 읽기 전용

    // Getter, Setter
    reversedMsg: {
      // 값을 얻어 냄
      get() {
        return this.msg.split("").reverse().join("");
      },
      // 값을 할당 함
      set(v) {
        this.msg = v;
      },
    },
  },
  methods: {
    add() {
      this.reversedMsg += "?!";
      // this.msg += "?!";
    },
  },
};
</script>

<style scoped>
h1 {
  font-size: 50px;
}

button {
  margin: 50px;
}
</style>
