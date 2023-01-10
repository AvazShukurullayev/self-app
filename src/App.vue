<template>
  <div id="app">
    <div class="container font-monospace py-3">
      <div class="content">
        <AppInfo
          :allMoviesLength="movies.length"
          :moviesFavouriteLength="movies.filter((c) => c.favourite).length"
          :moviesLikedLength="movies.filter((c) => c.like).length"
        />
        <MyBox class="search-panel">
          <SearchInput @onSearch="onSearchApp" />
          <FilterButtons />
        </MyBox>
        <MovieList
          :movies="onSearchMovies(movies, searchFromList)"
          @onLike="onLikeApp"
          @onFavourite="onFavouriteApp"
          @onRemove="onRemoveApp"
        />
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
      searchFromList: "",
    };
  },
  methods: {
    onSearchApp(param) {
      this.searchFromList = param;
    },
    onSearchMovies(arr, param) {
      if (param.length == 0) {
        return arr;
      }
      return (arr = this.movies.filter((c) =>
        c.title.toLowerCase().includes(this.searchFromList.toLowerCase())
      ));
    },
    movieAddItem(param) {
      this.movies.push(param);
    },
    onLikeApp(id) {
      this.movies = this.movies.map((element) => {
        if (element.id === id) {
          element.like = !element.like;
        }
        return element;
      });
    },
    onFavouriteApp(id) {
      this.movies = this.movies.map((element) => {
        if (element.id === id) {
          element.favourite = !element.favourite;
        }
        return element;
      });
    },
    onRemoveApp(id) {
      this.movies = this.movies.filter((c) => c.id !== id);
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
