<template>
  <MyBox class="app-info">
    <MyParag class="fs-3">Barcha kinolar soni: {{ allMoviesLength }}</MyParag>
    <MyParag class="fs-4">
      Favourite kinolar soni: {{ moviesFavouriteLength }}
    </MyParag>
    <MyParag class="fs-4">
      Liked kinolar soni: {{ moviesLikedLength }}
    </MyParag>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
import MyParag from "@/components/ui-components/MyParag.vue";
export default {
  name: "AppInfo",
  components: { MyBox, MyParag },
  props: ["allMoviesLength", "moviesFavouriteLength", "moviesLikedLength"],
  data() {
    return {};
  },
  methods: {},
};
</script>

<style></style>
