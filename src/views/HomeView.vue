<template>
  <center>
    <h1>Hello world!</h1>
  </center>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>

<style scoped>
center {
  background-image: url("@/assets/image.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 60vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

h1 {
  font-family: Arial, Helvetica, sans-serif;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
