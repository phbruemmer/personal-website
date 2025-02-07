<template>
  <div class="box-container">
    <h2 class="box-title">{{ title }}</h2>
    <p class="box-text"><slot /></p>
  </div>
</template>

<script>
export default {
  name: "LargeBox",
  props: {
    title: {
      type: String,
    },
  },
};
</script>

<style scoped>
.box-container {
  position: relative;
  width: 100%;
  max-width: 50%;
  margin: 20px auto;
  padding: 30px;
  background: #fffbf3;
  border-radius: 24px;
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.15);
  font-family: "Arial", sans-serif;
  transition: all 0.3s ease-in-out;
  transform: scale(1);
}

.box-title {
  font-size: 22px;
  color: #2c3e50;
  margin-bottom: 15px;
  text-align: center;
  font-weight: 700;
}

.box-text {
  font-size: 18px;
  color: #7f8c8d;
  text-align: center;
  line-height: 1.6;
  padding: 12px;
  margin-top: 10px;
}
</style>
