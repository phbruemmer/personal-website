<template>
  <MainHeader />
  <Welcome />
  <SectionSeperator id="Home"> Home </SectionSeperator>
  <Home />
  <SectionSeperator id="About"> About </SectionSeperator>
  <About />
  <SectionSeperator id="Projects"> Projects </SectionSeperator>
  <Projects />
  <SectionSeperator id="Prototypes"> Prototypes </SectionSeperator>
  <Prototypes />
  <Footer />
</template>

<script>
import MainHeader from "@/components/MainHeader/MainHeader.vue";
import Welcome from "@/components/MainPage/Welcome.vue";
import SectionSeperator from "@/components/Separators/SectionSeperator.vue";
import Home from "@/components/MainPage/Home/Home.vue";
import About from "@/components/MainPage/About/About.vue";
import Projects from "@/components/MainPage/Projects/Projects.vue";
import Prototypes from "@/components/MainPage/Prototypes/Prototypes.vue";
import Footer from "@/components/MainPage/Footer/Footer.vue";

export default {
  name: "HomeView",
  components: {
    MainHeader,
    Welcome,
    SectionSeperator,
    Home,
    Projects,
    About,
    Prototypes,
    Footer,
  },
};
</script>

<style scoped></style>
