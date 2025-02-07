<template>
  <Welcome />
  <SectionSeperator id="Home"> Home </SectionSeperator>
  <Home />
  <SectionSeperator id="About"> About </SectionSeperator>
  <SectionSeperator id="Projects"> Projects </SectionSeperator>
  <SectionSeperator id="Prototypes"> Prototypes </SectionSeperator>
</template>

<script>
import Welcome from "@/components/MainPage/Welcome.vue";
import SectionSeperator from "@/components/Separators/SectionSeperator.vue";
import Home from "@/components/MainPage/Home/Home.vue";

export default {
  name: "HomeView",
  components: {
    Welcome,
    SectionSeperator,
    Home,
  },
};
</script>

<style scoped></style>
