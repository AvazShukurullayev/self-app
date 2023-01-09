<template>
  <div class="btn-goup mt-3">
    <MyButton 
    v-for="filterBtn in filterButtons"
    class="btn-outline-dark"
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
          title: "En ko'p ko'rilgan kinolar",
          valueOfBtn: "mostViewers",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style></style>
