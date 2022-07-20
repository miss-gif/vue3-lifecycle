<template>
  <div class="btn">
    <slot></slot>
  </div>
  <h1 v-bind="$attrs">text</h1>
</template>

<script>
export default {
  inheritAttrs: false,
  created() {
    console.log(this.$attrs);
  },
};
</script>

<style lang="scss" scoped>
.btn {
  color: white;
  cursor: pointer;
  background-color: gray;
  display: inline-block;
  margin: 4px;
  padding: 60px 120px;
  border-radius: 4px;
  &.large {
    font-size: 20px;
    padding: 200px;
  }
}
</style>
