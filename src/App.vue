<template>
  <div id="app">
    <div class="container font-monospace py-3">
      <div class="content">
        <AppInfo
          :allMoviesLength="movies.length"
          :moviesFavouriteLength="movies.filter((c) => c.favourite).length"
        />
        <MyBox class="search-panel">
          <SearchInput />
          <FilterButtons />
        </MyBox>
        <MovieList :movies="movies" />
        <MovieAddForm @movieAddItem="movieAddItem" />
      </div>
    </div>
  </div>
</template>

<script>
import AppInfo from "@/components/app-info/AppInfo.vue";
import MyBox from "@/components/ui-components/MyBox.vue";
import SearchInput from "@/components/search-input/SearchInput.vue";
import FilterButtons from "@/components/filter-buttons/FilterButtons.vue";
import MovieList from "@/components/movie-list/MovieList.vue";
import MovieAddForm from "@/components/movie-add-form/MovieAddForm.vue";
export default {
  name: "App",
  components: {
    AppInfo,
    MyBox,
    SearchInput,
    FilterButtons,
    MovieList,
    MovieAddForm,
  },
  data() {
    return {
      movies: [
        {
          title: "Omar",
          viewers: 894,
          favourite: false,
          like: false,
          id: 1,
        },
        {
          title: "Empire of Osman",
          viewers: 1145,
          favourite: false,
          like: false,
          id: 2,
        },
        {
          title: "Ertugrul",
          viewers: 714,
          favourite: false,
          like: false,
          id: 3,
        },
        {
          title: "Abdulhamid II",
          viewers: 1748,
          favourite: false,
          like: false,
          id: 4,
        },
        {
          title: "Empire of Mog'ul",
          viewers: 455,
          favourite: false,
          like: false,
          id: 5,
        },
        {
          title: "Murad IV. Bagdad Fatihi",
          viewers: 314,
          favourite: false,
          like: false,
          id: 6,
        },
      ],
    };
  },
  methods: {
    movieAddItem(par) {
      this.movies.push(par);
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
