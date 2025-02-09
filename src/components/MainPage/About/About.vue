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
</template>

<script>
import Diagram from "@/components/MainPage/About/Diagram.vue";
import Box from "@/components/MainPage/Box.vue";
import Path from "@/components/MainPage/About/Path.vue";

export default {
  name: "About",
  components: {
    Diagram,
    Box,
    Path,
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
</style>
