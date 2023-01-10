<template>
  <input
    type="text"
    class="form-control"
    placeholder="Kinolarni qidirish..."
    v-model="searching"
  />
</template>

<script>
export default {
  name: "SearchInput",
  components: {},
  props: {},
  data() {
    return {
      searching: "",
    };
  },
  methods: {},
 /*  updated() {
    console.log("this.searching => ", this.searching);
  }, */
};
</script>

<style></style>
