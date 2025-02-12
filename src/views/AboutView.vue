<template>
  <DefaultHeader />
  <FrontPage />
</template>

<script>
import DefaultHeader from "@/components/DefaultHeader/DefaultHeader.vue";
import FrontPage from "@/components/AboutPage/FrontPage.vue";

export default {
  name: "AboutView",
  components: {
    DefaultHeader,
    FrontPage,
  },
};
</script>
