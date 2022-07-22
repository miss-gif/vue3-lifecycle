<template>
  <div class="btn">
    <slot name="text">text</slot>
    <slot name="icon">icon</slot>
  </div>
</template>

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
