<template>
    <input
      type="text"
      class="form-control"
      placeholder="Kinolarni qidirish..."
      @input="$emit('onSearch', $event.target.value)"
    />
</template>

<script>
export default {
  name: "SearchInput",
  components: {},
  props: {},
  data() {
    return {
      // searching: "",
    };
  },
  methods: {},
};
</script>

<style></style>
