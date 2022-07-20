<template>
  <MyBtn>banana</MyBtn>
  <MyBtn :color="color"> <span style="color: red">ppp</span></MyBtn>
  <MyBtn large color="green">Cherry</MyBtn>
  <MyBtn>abc</MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn";

export default {
  components: {
    MyBtn,
  },
  data() {
    return {
      color: "#000",
    };
  },
};
</script>
