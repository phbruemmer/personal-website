<template>
  <Welcome />
  <SectionSeperator />
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
