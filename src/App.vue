<template>
  <MyBtn @heropy="log" @change-msg="logMsg">banana</MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn";

export default {
  components: {
    MyBtn,
  },
  methods: {
    log(event) {
      console.log("Click!!");
      console.log(event);
    },
    logMsg(msg) {
      console.log(msg);
    },
  },
};
</script>
