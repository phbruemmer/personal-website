<template>
  <div class="about-container">
    <div class="left-container">
      <Path />
    </div>
    <div class="right-container">
      <Box title="Programming Languages">
        <div class="centered">
          <div class="row">
            <Diagram progress="78">Python</Diagram>
            <Diagram progress="52">C++</Diagram>
          </div>
        </div>
        <a href="">Show more</a>
      </Box>

      <Box title="Software Development Areas">
        <div class="centered">
          <div class="row">
            <Diagram progress="68">Networking & communication</Diagram>
            <Diagram progress="45">Game Development</Diagram>
          </div>
        </div>
        <a href="">Show more</a>
      </Box>
    </div>
  </div>

  <DefaultSeperator />

  <div class="centered-button">
    <Visuals
      image-height="18vh"
      :first_path="require('@/assets/images/image (6).jpg')"
      :second_path="require('@/assets/images/image (12).jpg')"
      :third_path="require('@/assets/images/image (10).jpg')"
    />
    <button @click="$router.push('/about')">Show more!</button>

    <Visuals
      image-height="18vh"
      :first_path="require('@/assets/images/image (5).jpg')"
      :second_path="require('@/assets/images/image (3).jpg')"
      :third_path="require('@/assets/images/image (11).jpg')"
    />
  </div>
  <DefaultSeperator />
</template>

<script>
import Diagram from "@/components/MainPage/About/Diagram.vue";
import Box from "@/components/MainPage/Box.vue";
import Path from "@/components/MainPage/About/Path.vue";
import Visuals from "@/components/MainPage/Visuals.vue";
import DefaultSeperator from "@/components/Separators/DefaultSeperator.vue";

export default {
  name: "About",
  components: {
    Diagram,
    Box,
    Path,
    Visuals,
    DefaultSeperator,
  },
};
</script>

<style scoped>
.about-container {
  display: flex;
  justify-content: space-around;
  align-items: stretch;
}

.left-container,
.right-container {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.right-container {
  gap: 20px;
}

.centered {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.row {
  display: flex;
  gap: 40px;
  justify-content: center;
}

a {
  color: #616161;
  font-family: Arial, Helvetica, sans-serif;
}

.left-container {
  display: flex;
  align-items: center;
  justify-content: center;
}

.centered-button {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-top: 6vh;
  margin-bottom: 4vh;
  background-color: #fae3b43a;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  border-radius: 40px;
  margin-left: 20vb;
  margin-right: 20vb;
  height: 30vh;
  transition: box-shadow 0.3s ease-in-out;
}

.centered-button:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4);
}

button {
  padding: 1.25em 3.75em;
  background-color: #fffbf3;
  border: none;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
  border-radius: 16px;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1em;
  font-weight: 100;
  transition: background-color 0.2s ease-in-out, transform 0.15s ease-in-out,
    box-shadow 0.2s ease-in-out;
}

button:hover {
  background-color: #f1ece2;
  transform: translateY(-2px);
  box-shadow: 0 12px 20px rgba(0, 0, 0, 0.15);
}

button:active {
  background-color: #e6e0d5;
  transform: translateY(1px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
}
</style>
