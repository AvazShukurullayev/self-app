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
};
</script>

<style></style>
