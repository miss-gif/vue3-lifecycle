<template>
  <div :class="{ large }" :style="{ backgroundColor: color }" class="btn">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "gray",
    },
    large: {
      type: Boolean,
      default: false,
    },
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
