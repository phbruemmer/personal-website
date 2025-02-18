<template>
  <div class="">
    <Box title="Introduction">
      <b>Hey there!</b> <br />Welcome to my portfolio. Check out my
      <a href="/" class="no-underline">latest work</a>! You can reach out to me
      via <a href="/" class="no-underline">Discord</a>,
      <a href="/" class="no-underline">email</a> or the integrated messaging
      tool
      <a href="https://discordapp.com" target="_blank" rel="noopener noreferrer"
        >here</a
      >.
    </Box>
  </div>
</template>

<script>
import Box from "@/components/AboutPage/Box.vue";

export default {
  name: "Content",
  components: {
    Box,
  },
};
</script>

<style scoped>
a {
  color: #fff;
}

.no-underline {
  text-decoration: none;
}
.no-underline:hover {
  text-decoration: underline;
}
</style>
