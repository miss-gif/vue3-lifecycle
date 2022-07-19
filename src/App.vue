<template>
  <button @click="handler">Click me! 1</button>
  <button @click="handler('hi')">Click me! 2</button>
  <button @click="handler('what')">Click me! 3</button>
  <button @click="handler('ai', $event)">Click me! 4</button>
</template>

<script>
export default {
  methods: {
    handler(event) {
      console.log(event);
      console.log(event.target);
      console.log(event.target.textContent);
    },
    handler(msg) {
      console.log(msg);
    },
    handler(msg, event) {
      console.log(msg);
      console.log(event);
    },
  },
};
</script>
