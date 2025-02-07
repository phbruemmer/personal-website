<template>
  <div class="project-container">
    <div class="left-container">
      <img :src="path" alt="Project Image" />
    </div>

    <div class="right-container">
      <h1>{{ title }}</h1>
      <p>
        <slot />
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: {
    title: {
      type: String,
      required: false,
    },
    path: {
      type: String,
      required: false,
    },
  },
};
</script>

<style scoped>
.project-container {
  margin-top: 40px;
  display: flex;
  justify-content: space-between;
  background-color: #fce8e8;
  align-items: center;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.left-container {
  flex: 1;
  display: flex;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 20px;
}

img {
  height: 100px;
  width: auto;
  margin-left: 20px;
  object-fit: cover;
  border-radius: 16px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out;
}

img:hover {
  transform: scale(1.05);
}

.right-container {
  flex: 2;
}

h1 {
  font-size: 20px;
  font-weight: 600;
  color: #565656;
}

p {
  font-size: 16px;
  color: #666;
  line-height: 1.5;
  text-align: center;
  margin-right: 20px;
}
</style>
