<template>
  <DefaultHeader />
  <FrontPage />
  <Content />
</template>

<script>
import DefaultHeader from "@/components/DefaultHeader/DefaultHeader.vue";
import FrontPage from "@/components/AboutPage/FrontPage.vue";
import Content from "@/components/AboutPage/Content.vue";

export default {
  name: "AboutView",
  components: {
    DefaultHeader,
    FrontPage,
    Content,
  },
};
</script>
