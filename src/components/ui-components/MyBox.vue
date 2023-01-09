<template>
  <div class="box">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "MyBox",
};
</script>

<style>
.box {
  margin: 1.5rem 0;
  padding: 1.5rem;
  box-shadow: 3px 3px 15px rgba(0, 0, 0, 0.15);
  border-radius: 6px;
  background-color: #fffafaef;
}
</style>
