<template>
  <Welcome />
  <SectionSeperator id="Home"> Home </SectionSeperator>
  <SectionSeperator id="About"> About </SectionSeperator>
  <SectionSeperator id="Projects"> Projects </SectionSeperator>
  <SectionSeperator id="Prototypes"> Prototypes </SectionSeperator>
</template>

<script>
import Welcome from "@/components/MainPage/Welcome.vue";
import SectionSeperator from "@/components/Separators/SectionSeperator.vue";

export default {
  name: "HomeView",
  components: {
    Welcome,
    SectionSeperator,
  },
};
</script>

<style scoped></style>
