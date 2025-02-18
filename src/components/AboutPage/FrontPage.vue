<template>
  <div class="container">
    <div class="center">
      <div class="overlay"></div>
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
.container {
  position: relative;
  text-align: center;
  color: white;
}

.center {
  margin-top: 2vh;
  background-image: url("@/assets/images/image (12).jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 50vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
  transition: box-shadow 0.3s ease-in-out;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

h1 {
  font-size: 64px;
  font-weight: bold;
  z-index: 1;
  position: relative;
  transition: transform 0.3s ease-in-out;
}

h1:hover {
  transform: scale(1.05);
  cursor: default;
}
</style>
