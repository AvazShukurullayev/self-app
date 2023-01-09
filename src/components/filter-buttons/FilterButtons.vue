<template>
  <div class="btn-goup">
    <MyButton>Barcha kinolar</MyButton>
    <MyButton>Mashxur kinolar</MyButton>
    <MyButton>Eng ko'p ko'rilgan kinolar</MyButton>
  </div>
</template>

<script>
import MyButton from "@/components/ui-components/MyButton.vue";
export default {
  name: "FilterButtons",
  components: { MyButton },
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style></style>
