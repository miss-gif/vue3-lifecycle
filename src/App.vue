<template>
  <div class="parent" @click.self="handlerA">
    <div class="child"></div>
  </div>
</template>

<script>
export default {
  methods: {
    handlerA() {
      console.log("A");
    },
    handlerB() {
      console.log("B");
    },
  },
};
</script>

<style lang="scss">
.parent {
  width: 200px;
  height: 200px;
  background-color: rebeccapurple;
}
.child {
  width: 100px;
  height: 100px;
  background-color: burlywood;
}
</style>
