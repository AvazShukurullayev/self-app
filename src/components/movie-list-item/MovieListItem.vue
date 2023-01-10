<template>
  <li class="movie-list-item">
    <span class="movie-list-item-label">{{ movie.title }}</span>
    <div class="movie-list-item-content d-flex align-items-center">
      <input
        type="number"
        class="movie-list-item-input form-control text-center"
        :value="movie.viewers"
      />
      <button class="btn-cookie btn-sm">
        <i class="fas fa-cookie"></i>
      </button>
      <button class="btn-trash btn-sm">
        <i class="fas fa-trash"></i>
      </button>
      <i class="fas fa-star"></i>
    </div>
  </li>
</template>

<script>
export default {
  name: "MovieListItem",
  props: ["movie"],
  comments: {},
};
</script>

<style>
.movie-list-item-label {
  font-size: 20px;
  padding: 5px 0;
  max-width: 550px;
  width: 100%;
  cursor: pointer;
}
.btn-cookie,
.btn-trash {
  background-color: #e9e7e7;
  margin: 3px 5px;
  width: 35px;
  height: 35px;
}
.btn-cookie {
  color: orange;
}
.btn-cookie:hover {
  color: orange;
  background-color: #b6b6b69a;
}
.btn-trash {
  color: orangered;
}
.btn-trash:hover {
  color: orangered;
  background-color: #b6b6b69a;
}
.fa-star {
  width: 40px;
  color: gold;
  opacity: 0;
  transform: translateX(20px);
  transition: all 0.3s;
}
.movie-list-item.like .fa-star {
  opacity: 1;
  transform: translateX(0);
}
.movie-list-item.favourite .movie-list-item-label,
.movie-list-item.favourite .movie-list-item-input {
  color: gold;
}
</style>
