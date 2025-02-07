<template>
  <div class="home-container">
    <div class="box-container">
      <Box title="~ Welcome ~">
        Hi, I'm <i>Philip</i>, a self-taught developer from <b>Germany</b>,
        passionate about problem-solving and computers in general. Furthermore,
        I enjoy working on challenging projects and exploring a variety of
        technologies.
      </Box>

      <Box title="~ What I do ~">
        As a self-taught developer, I currently focus on my own projects, but
        I'm always seeking new challenges that help me grow and collaborate with
        others in the ever-evolving world of tech. Explore my
        <DefaultLink reference="About">journey</DefaultLink> and the
        <DefaultLink reference="Projects">projects</DefaultLink> I'm working on.
      </Box>
    </div>

    <div class="content-container">
      <Visuals
        :first_path="require('@/assets/images/image (0).jpg')"
        :second_path="require('@/assets/images/image (6).jpg')"
        :third_path="require('@/assets/images/image (4).jpg')"
      />
    </div>
  </div>

  <!-- Please add hot chocolate icons. -->
</template>

<script>
import Box from "@/components/MainPage/Box.vue";
import DefaultLink from "@/components/DefaultLink.vue";
import Visuals from "@/components/MainPage/Home/Visuals.vue";

export default {
  name: "Home",
  components: {
    Box,
    DefaultLink,
    Visuals,
  },
};
</script>

<style scoped>
.home-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
