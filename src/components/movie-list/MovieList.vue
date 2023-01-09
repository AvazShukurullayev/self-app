<template>
    <MyBox>
        <ul>
          <li>Omar</li>
          <li>Empire of Osman</li>
          <li>Ertugrul</li>
        </ul>
    </MyBox>
</template>

<script>
import MyBox from '../ui-components/MyBox.vue';
export default {
  name: "MovieList",
  components: {MyBox},
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style></style>
