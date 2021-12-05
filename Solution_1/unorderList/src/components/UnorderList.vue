<template>
  <div class="list">
    <ul>
      <li v-for="(numbers, index) in 101" :key="index">
        <div v-if="divisible(numbers + offset)">
          {{ numbers + offset }}
          <div class="result">{{ divisible(numbers + offset) }}</div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "UnorderList",
data() {
  return {
    offset: 2
  }
},
  methods: {
    divisible(num) {
      /* eslint-disable no-mixed-spaces-and-tabs */
      if (num % 3 === 0 && num % 5 === 0) {
        return "three and five";
      }
      if (num % 3 === 0) {
        return "three";
      }
      if (num % 5 === 0) {
        return "five";
      }
      return null;
      /* eslint-enable no-mixed-spaces-and-tabs */
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
.list {
  display: flex;
  justify-content: center;
}

ul {
  list-style-type: none;
}

li div {
  border-radius: 5px;
  font-size: 2rem;
  display: flex;
  justify-content: flex-end;
  padding: 0.5rem;
  margin-bottom: 1rem;
  background-color: rgb(163, 163, 163);
  width: 33rem;
  align-items: center;
}
</style>
