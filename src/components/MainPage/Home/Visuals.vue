<template>
  <div class="gallery-container">
    <div class="image-wrapper">
      <img :src="first_path" class="image" />
    </div>
    <div class="image-wrapper">
      <img :src="second_path" class="image" />
    </div>
    <div class="image-wrapper">
      <img :src="third_path" class="image" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Visuals",
  props: {
    first_path: {
      type: String,
      required: true,
    },
    second_path: {
      type: String,
      required: true,
    },
    third_path: {
      type: String,
      required: true,
    },
  },
  mounted() {
    console.log(this.fir);
  },
};
</script>

<style scoped>
.gallery-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 15px;
  margin-top: 20px;
}

.image-wrapper {
  position: relative;
  width: 150px;
  height: 300px;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  transition: transform 0.2s ease, box-shadow 0.3s ease;
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease, opacity 0.3s ease;
}

.image-wrapper:hover {
  transform: scale(1.05);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
}

.image-wrapper:hover .image {
  transform: scale(1.05);
  opacity: 0.9;
}
</style>
