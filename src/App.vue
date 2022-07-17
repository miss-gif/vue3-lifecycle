<template>
  <h1 @click="changeMsg">{{ msg }}</h1>
  <h1>{{ reversedMsg }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello???",
    };
  },
  computed: {
    reversedMsg() {
      return this.msg.split("").reverse().join("");
    },
  },
  // 변경되는 사항을 감지
  watch: {
    // msg() {
    //   console.log("msg:", this.msg);
    // },
    msg(value) {
      console.log("msg:", value);
    },
    reversedMsg() {
      console.log("reversedMsg:", this.reversedMsg);
    },
  },
  methods: {
    changeMsg() {
      this.msg = "Good!!!!!!!";
    },
  },
};
</script>
