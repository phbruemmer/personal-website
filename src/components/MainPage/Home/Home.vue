<template>
  <Box title="~ Welcome ~">
    Hi, I'm <i>Philip</i>, a self-taught developer from <b>Germany</b>,
    passionate about problem-solving and computers in general. Furthermore, I
    enjoy working on challenging projects and exploring a variety of
    technologies.
  </Box>

  <Box title="~ What I do ~">
    As a self-taught developer, I currently focus on my own projects, but I'm
    always seeking new challenges that help me grow and collaborate with others
    in the ever-evolving world of tech. Explore my
    <DefaultLink reference="About">journey</DefaultLink> and the
    <DefaultLink reference="Projects">projects</DefaultLink> I'm working on.
  </Box>
</template>

<script>
import Box from "@/components/MainPage/Box.vue";
import DefaultLink from "@/components/DefaultLink.vue";

export default {
  name: "Home",
  components: {
    Box,
    DefaultLink,
  },
};
</script>

<style scoped></style>
