<template>
  <MyBox class="app-info">
    <MyParag class="fs-3">Barcha kinolar soni: 0</MyParag>
    <MyParag class="fs-4">Favourite kinolar soni: 0</MyParag>
  </MyBox>
</template>

<script>
import MyBox from "../ui-components/MyBox.vue";
import MyParag from "../ui-components/MyParag.vue";
export default {
  name: "AppInfo",
  components: { MyBox,MyParag },
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style></style>
