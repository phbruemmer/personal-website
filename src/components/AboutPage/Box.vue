<template>
  <div class="box">
    <div class="title">
      <h1>~ {{ title }} ~</h1>
    </div>
    <div class="content">
      <p><slot /></p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Box",
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.box {
  background-color: #131e3b;
  max-width: 500px;
  width: 90%;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  text-align: center;
  margin: 20px auto;
}

.box:hover {
  cursor: default;
}

.title {
  padding: 15px;
}

h1 {
  font-size: 32px;
  font-weight: bold;
  margin: 0;
  background: linear-gradient(135deg, #00a8cc, #00feba, #00a8cc);
  background-size: 200% 200%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradientMove 3s linear infinite;
  display: inline-block;
}

@keyframes gradientMove {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.content {
  display: flex;
  justify-content: center;
  padding: 20px;
}

p {
  color: #e0e0e0;
  font-size: 18px;
  line-height: 1.5;
}
</style>
