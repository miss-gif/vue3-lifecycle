<template>
  <ul>
    <li v-for="fruit in newFriuits" :key="fruit.id">
      {{ fruit.name }}
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
      return this.fruits.map((fruit, index) => {
        return {
          id: index,
          name: fruit,
        };
      });
    },
  },
};
</script>
