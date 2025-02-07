<template>
  <LargeBox title="~ featured projects ~">
    <Project title="HTTP-Server" :path="require('@/assets/projects/HTTP.png')"
      >This project is an HTTP server built with Python sockets, offering
      features like view handling, URL routing, static file support, and
      JavaScript handling. It also supports database connections for data
      storage, making it a lightweight web framework.</Project
    >
    <Project title="HTTP-Server" :path="require('@/assets/projects/HTTP.png')"
      >This project is an HTTP server built with Python sockets, offering
      features like view handling, URL routing, static file support, and
      JavaScript handling. It also supports database connections for data
      storage, making it a lightweight web framework.</Project
    >
  </LargeBox>
</template>

<script>
import LargeBox from "@/components/MainPage/LargeBox.vue";
import Project from "@/components/MainPage/Project.vue";

export default {
  name: "Projects",
  components: {
    LargeBox,
    Project,
  },
};
</script>

<style scoped></style>
