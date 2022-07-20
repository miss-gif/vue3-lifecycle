<template>
  <div class="btn">
    <slot></slot>
  </div>
  <h1 @dblclick="$emit('heropy', $event)">text</h1>
  <input type="text" v-model="msg" />
</template>

<script>
export default {
  emits: ["heropy", "changeMsg"],
  data() {
    return {
      msg: "",
    };
  },
  watch: {
    msg() {
      this.$emit("changeMsg", this.msg);
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
