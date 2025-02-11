<template>
  <div class="link-container">
    <a @click.prevent="$router.push(reference)"><slot /></a>
  </div>
</template>

<script>
export default {
  name: "RouterLinks",
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
  margin-right: 80px;
  font-size: 18px;
  font-weight: 100;
  font-family: Arial, Helvetica, sans-serif;
  display: inline-block;
  position: relative;
  text-decoration: none;
  color: #000;
}

a::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #000;
  transition: width 0.2s ease;
}

a:hover::after {
  width: 100%;
}

a:hover {
  cursor: pointer;
}
</style>
