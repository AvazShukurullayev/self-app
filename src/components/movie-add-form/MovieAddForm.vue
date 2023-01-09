<template>
  <MyBox>
    <h3 class="movie-add-form__title">Kinolar qo'shish</h3>
    <form class="d-flex" @submit.prevent="onSubmitMovieAddForm">
      <input
        class="form-control"
        type="text"
        placeholder="Kinoning nomi?"
        required
        v-model="form.title"
      />
      <input
        class="form-control"
        type="number"
        placeholder="Necha marotaba ko'rilgan?"
        required
        v-model="form.viewers"
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
      console.log(this.form.title);
      console.log(this.form.viewers);
    },
  },
};
</script>

<style>
.movie-add-form__title {
  margin-bottom: 1rem;
}
</style>
