<template>
  <div class="rating-container">
    <div
      v-for="(s, idx) in stars"
      :key="idx"
      class="star"
      v-bind:class="{ filled: s }"
    />
  </div>
</template>

<script>
export default {
  name: "StarRating",
  props: {
    ratio: Number,
  },
  computed: {
    stars() {
      const arr = new Array(5).map(() => false);

      for (let i = 0; i < this.ratio; i++) {
        arr[i] = true;
      }
      return arr;
    },
  },
};
</script>

<style>
.rating-container {
  display: flex;
  justify-content: flex-start;
}
.rating-container * {
  box-sizing: border-box;
}
.rating-container .star {
  width: 50px;
  height: 50px;
  background-image: url("../assets/star.png");
  background-size: cover;
  background-position: 10% 0%;
}
.rating-container .star.filled {
  background-position: 90% 0%;
}
</style>
