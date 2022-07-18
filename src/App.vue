<template>
  <button @click="handler">click me!</button>
  <ul>
    <li v-for="{ id, name } in newFriuits" :key="id">
      {{ name }} --- {{ id }}
    </li>
  </ul>
</template>

<script>
import shortid from "shortid";

export default {
  data() {
    return {
      fruits: ["Apple", "Banana", "Cherry"],
    };
  },
  computed: {
    newFriuits() {
      return this.fruits.map((fruit) => ({
        id: shortid.generate(),
        name: fruit,
      }));
    },
  },
  methods: {
    handler() {
      this.fruits.push("Orange");
    },
  },
};
</script>
