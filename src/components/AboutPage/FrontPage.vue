<template>
  <div class="container">
    <div class="center">
      <h1>~ About ~</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "FrontPage",
};
</script>

<style scoped>
h1 {
  font-size: 64px;
  color: #fff;
}

.center {
  margin-top: 2vh;
  background-image: url("@/assets/images/image (12).jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 40vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2), 0 -10px 20px rgba(0, 0, 0, 0.2);
  transition: box-shadow 0.3s ease-in-out;
}

.center:hover {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3), 0 -10px 20px rgba(0, 0, 0, 0.3);
}

h1 {
  transition: transform 0.3s ease-in-out;
}

h1:hover {
  cursor: default;
  transform: scale(1.05);
}

.container {
  position: relative;
}
</style>
