<template>
  <div class="social-container">
    <Social
      logo_path="https://th.bing.com/th/id/R.57e3e076a3eebb2b667d325b425e717a?rik=uHVdR7Kz%2bpTxVw&pid=ImgRaw&r=0"
    />

    <Social
      logo_path="https://mir-s3-cdn-cf.behance.net/project_modules/disp/f8dc5431091769.5640f77be5837.png"
    />

    <Social
      logo_path="https://th.bing.com/th/id/R.32c6d327568ffba8f0fe563a0471a1d0?rik=YEbiLMkUlcjKWA&pid=ImgRaw&r=0"
    />
  </div>
</template>

<script>
import Social from "@/components/MainHeader/Social.vue";

export default {
  name: "SocialNavbar",
  components: {
    Social,
  },
};
</script>

<style scoped>
.social-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
