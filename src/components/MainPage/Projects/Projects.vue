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

<style scoped></style>
