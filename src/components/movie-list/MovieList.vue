<template>
  <MyBox>
    <ul class="list-group">
      <MovieListItem
        v-for="movie in movies"
        :key="movie.id"
        :movie="movie"
        :class="{ like: movie.like, favourite: movie.favourite }"
      />
    </ul>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";

import MovieListItem from "../movie-list-item/MovieListItem.vue";
export default {
  name: "MovieList",
  components: { MyBox, MovieListItem },
  props: ["movies"],
  data() {
    return {};
  },
  methods: {
    onFavourite() {
      console.log("onFavourite");
    },
    onRemove() {
      console.log("onRemove");
    },
  },
};
</script>

<style></style>
