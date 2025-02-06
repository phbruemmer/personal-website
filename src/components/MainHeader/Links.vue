<template>
  <div class="link-container">
    <a :href="reference"><slot /></a>
  </div>
</template>

<script>
export default {
  name: "Links",
  props: {
    reference: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: #000;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: 100;
  font-size: 16px;
  margin: 10px;
}
</style>
