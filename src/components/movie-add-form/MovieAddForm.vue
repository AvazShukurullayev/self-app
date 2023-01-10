<template>
  <MyBox>
    <h3 class="movie-add-form__title">Kino qo'shish</h3>
    <form class="d-flex" @submit.prevent="onSubmitMovieAddForm">
      <input
        class="form-control"
        type="text"
        placeholder="Kinoning nomi?"
        v-model="form.title"
        required
      />
      <input
        class="form-control"
        type="number"
        placeholder="Necha marotaba ko'rilgan?"
        v-model="form.viewers"
        required
      />
      <MyButton class="btn-outline-dark" type="submit">Qo'shish</MyButton>
    </form>
  </MyBox>
</template>

<script>
import MyBox from "@/components/ui-components/MyBox.vue";
import MyButton from "@/components/ui-components/MyButton.vue";
export default {
  name: "MovieAddForm",
  components: { MyBox, MyButton },
  props: {},
  data() {
    return {
      form: {},
    };
  },
  methods: {
    onSubmitMovieAddForm() {
      if (this.form.title !== "" && this.form.viewers !== "") {
        const newMovieItem = {
          title: this.form.title,
          viewers: this.form.viewers,
          favourite: false,
          like: false,
          id: Date.now(),
        };
        this.$emit("movieAddItem", newMovieItem);
        this.form = {};
      } else {
        return alert("Movie-add-form da xatolik bor");
      }
    },
  },
};
</script>

<style>
.movie-add-form__title {
  margin-bottom: 1rem;
}
</style>
