<template>
  <MyBox>
    <h2 class="title">Kinolar qo'shish</h2>
    <form>
      <input type="text" />
      <input type="number" />
      <button type="submit">Qo'shish</button>
    </form>
  </MyBox>
</template>

<script>
import MyBox from "../ui-components/MyBox.vue";
export default {
  name: "MovieAddForm",
  components: { MyBox },
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style></style>
