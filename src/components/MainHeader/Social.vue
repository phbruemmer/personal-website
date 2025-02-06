<template>
  <div class="social-container">
    <!-- clickable logo -->
    <img :src="logo_path" />
  </div>
</template>

<script>
export default {
  name: "Social",
  props: {
    logo_path: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
img {
  width: 100px;
  height: auto;
}
</style>
