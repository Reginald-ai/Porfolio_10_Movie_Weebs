<template>
  <div class="home">
    <Navbar />
    <section class="row">
      <NavbarSide />
      <MovieList />
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "../components/Navbar.vue";
import NavbarSide from "../components/NavbarSide.vue";
import MovieList from "../components/MovieList.vue";

export default {
  name: "Home",
  data() {
    return {};
  },
  components: {
    Navbar,
    NavbarSide,
    MovieList,
  },
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins&family=Quicksand&display=swap");
body {
  background: #393939 !important;
  height: 100vh;
  font-family: "Poppins", sans-serif;
  font-family: "Quicksand", sans-serif;
}
section {
  display: flex;
}
</style>
