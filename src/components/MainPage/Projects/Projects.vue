<template>
  <LargeBox title="~ featured projects ~">
    <Project title="HTTP-Server" :path="require('@/assets/projects/HTTP.png')"
      >This project is an HTTP server built with Python sockets, offering
      features like view handling, URL routing, static file support, and
      JavaScript handling. It also supports database connections for data
      storage, making it a lightweight web framework.</Project
    >
    <Project title="Bank-Server" :path="require('@/assets/projects/bank.webp')"
      >Lazarus Bank System handles deposits, transfers, checks, and currency
      exchange. A Lazarus client connects via TCP to a Python server with a JSON
      database that handles all the interactions. All transactions run
      insecurely on the server side.</Project
    >
  </LargeBox>

  <div class="seperator">
    <div class="left-container">
      <img src="@/assets/coffee.png" alt="" />
    </div>

    <div class="right-container">
      <img src="@/assets/coffee.png" alt="" />
    </div>
  </div>

  <LargeBox title="~ current projects ~">
    <Project
      title="personal website"
      bg-color="#e8fceb"
      :path="require('@/assets/projects/current_project.png')"
      >A personal website built with Vue.js. Future plans include integrating a
      Django backend to handle data management, authentication, creating a
      full-stack web application.</Project
    >
  </LargeBox>
</template>

<script>
import LargeBox from "@/components/MainPage/LargeBox.vue";
import Project from "@/components/MainPage/Projects/Project.vue";

export default {
  name: "Projects",
  components: {
    LargeBox,
    Project,
  },
};
</script>

<style scoped>
.seperator {
  display: flex;
  justify-content: space-around;
  align-items: center;
  gap: 60%;
  position: relative;
  margin-top: 30px;
}

.seperator::after {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%);
  width: 60%;
  border-top: 3px dotted #b19873b5;
}

.left-container {
  background-color: #ead4b2;
  padding: 10px;
  border-radius: 50%;
  border: 3px dotted #b1987386;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 180px;
  height: 180px;
  transition: transform 0.3s ease-in-out;
}

.right-container {
  background-color: #ead4b2;
  padding: 10px;
  border-radius: 50%;
  border: 3px dotted #b1987386;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 180px;
  height: 180px;
  transition: transform 0.3s ease-in-out;
}

.left-container:hover {
  transform: scale(0.95);
}

.right-container:hover {
  transform: scale(0.95);
}

.left-container img {
  width: 125px;
  height: auto;
  border: none;
  margin: 0;
  transform: rotate(5deg);
  transition: transform 0.3s ease;
}

.left-container img:hover {
  transform: rotate(-15deg);
}

.right-container img {
  width: 125px;
  height: auto;
  border: none;
  margin: 0;
  transform: rotate(-5deg);
  transition: transform 0.3s ease;
}

.right-container img:hover {
  transform: rotate(15deg);
}

img {
  opacity: 0.8;
}
</style>
