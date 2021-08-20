<template>
  <div class="movies-container col-md-9">
    <div class="row">
      <Movie v-for="movie in movies" :key="movie.id" :movie="movie" />
    </div>
  </div>
</template>

<script>
import Movie from "./Movie.vue";
export default {
  components: {
    Movie,
  },

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
  color: #fff;
}
</style>
