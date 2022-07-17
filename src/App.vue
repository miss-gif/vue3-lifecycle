<template>
  <h1 v-once @click="add">{{ msg }}</h1>
  <h1 v-bind:class="active">{{ msg2 }}</h1>
  <h1 :[attr]="'active'" @click="add"> {{ msg2 }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world',
      msg2: 'active',
      attr: 'class',
      event: 'click'
    }
  },
  methods: {
    add() {
      this.msg2 += '!'
    }
  }
}
</script>

<style scoped>
.active {
  font-size: 100px;
  color: blueviolet;
}
</style>