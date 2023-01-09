<template>
  <div id="app">
    <div class="container font-monospace py-3">
      <div class="content">
        <AppInfo />
        <MyBox class="search-panel">
          <h2>Search Input</h2>
          <h2>Filter buttons</h2>
        </MyBox>
        <h2>Movie list</h2>
        <h2>Movie add form</h2>
      </div>
    </div>
  </div>
</template>

<script>
import AppInfo from "./components/app-info/AppInfo.vue";
import MyBox from "@/components/ui-components/MyBox.vue";
export default {
  name: "App",
  components: { AppInfo, MyBox },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss">
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
