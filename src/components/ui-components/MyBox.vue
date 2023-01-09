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
  margin: 1rem 0;
  padding: 1rem;
  box-shadow: 15px 15px 15px rgba(0, 0, 0, 0.15);
  border-radius: 6px;
  background-color: #f8f8f8c2;
}
</style>
