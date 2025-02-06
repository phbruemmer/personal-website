<template>
  <div class="logo-container">
    <img src="@/assets/signature.png" alt="logo" />
  </div>
</template>

<script>
export default {
  name: "Logo",
};
</script>

<style scoped>
.logo-container {
  margin-left: 20px;
  display: flex;
  width: 200px;
}
img {
  width: 150px;
  height: auto;
}
</style>
