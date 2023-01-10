<template>
  <div class="btn-goup mt-3">
    <MyButton
      v-for="filterBtn in filterButtons"
      :key="filterBtn.title"
      @click="onFilterClick(filterBtn.valueOfBtn)"
      :class="[
        filter == filterBtn.valueOfBtn ? 'btn-dark' : 'btn-outline-dark',
      ]"
    >
      {{ filterBtn.title }}
    </MyButton>
  </div>
</template>

<script>
import MyButton from "@/components/ui-components/MyButton.vue";
export default {
  name: "FilterButtons",
  components: { MyButton },
  props: {},
  data() {
    return {
      filterButtons: [
        {
          title: "Barcha kinolar",
          valueOfBtn: "all",
        },
        {
          title: "Mashhur kinolar",
          valueOfBtn: "popular",
        },
        {
          title: "Eng ko'p ko'rilgan kinolar",
          valueOfBtn: "mostViewers",
        },
      ],
      filter: "all",
    };
  },
  methods: {
    onFilterClick(par) {
      this.filter = par;
      this.$emit("onFilterButton", this.filter);
    },
  },
};
</script>

<style></style>
