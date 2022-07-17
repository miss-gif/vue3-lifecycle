<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 2,
    };
  },
  // 컴포넌트 생성 직전, 활용도 낮음
  beforeCreate() {
    console.log("before Create", this.count);
  },
  // 컴포넌트 생성 직후
  created() {
    console.log("Created!", this.count);
  },
  // html 연결 전, 활용도 낮음
  beforeMount() {
    console.log("before Mount");
    console.log(document.querySelector("h1"))
  },
  // html 연결 후
  mounted() {
    console.log("mounted!");
    console.log(document.querySelector("h1"))
  },
};
</script>
