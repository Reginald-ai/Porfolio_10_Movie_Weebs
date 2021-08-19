<template>
  <div class="movies-container">
    <h1>Movies</h1>
    <ul>
      <li v-for="(movie, index) in movies" :key="movie.id">
        index:{{ index }} {{ movie.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  computed: {
    movies() {
      return this.$store.getters.getMovies;
    },
  },
  methods: {},
};
</script>

<style>
.movies-container {
  padding: 40px;
  color: #fff;
}
</style>
