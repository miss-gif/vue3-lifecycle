<template>
  <h1 @click="increase">
    {{ count }}
  </h1>
  <div v-if="count > 4">4보다 큽니다!</div>
  <ul>
    <Fruit v-for="fruit in fruits" :key="fruit" :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>

<script>
import Fruit from "~/components/Fruit";
export default {
  components: {
    Fruit,
  },
  data() {
    return {
      count: 0,
      fruits: ["사과", "바나나", "체리"],
    };
  },
  methods: {
    increase() {
      this.count += 1;
    },
  },
};
</script>
