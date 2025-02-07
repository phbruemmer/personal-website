<template>
  <Welcome />
  <SectionSeperator id="Home"> Home </SectionSeperator>
  <Home />
  <SectionSeperator id="About"> About </SectionSeperator>
  <About />
  <SectionSeperator id="Projects"> Projects </SectionSeperator>
  <Projects />
  <SectionSeperator id="Prototypes"> Prototypes </SectionSeperator>
</template>

<script>
import Welcome from "@/components/MainPage/Welcome.vue";
import SectionSeperator from "@/components/Separators/SectionSeperator.vue";
import Home from "@/components/MainPage/Home/Home.vue";
import About from "@/components/MainPage/About/About.vue";
import Projects from "@/components/MainPage/Projects/Projects.vue";

export default {
  name: "HomeView",
  components: {
    Welcome,
    SectionSeperator,
    Home,
    Projects,
    About,
  },
};
</script>

<style scoped></style>
