<template>
  <div class="social-container">
    <a href="https://github.com/phbruemmer"
      ><img src="@/assets/socials/github.svg" />
    </a>

    <a href="https://www.instagram.com/phbruemmer/">
      <img src="@/assets/socials/instagram.svg" />
    </a>

    <a href="https://x.com/1Phbruemmer">
      <img src="@/assets/socials/x.svg" />
    </a>

    <a href="https://discord.gg/a2h5feJ8aV">
      <img src="@/assets/socials/discord.svg" />
    </a>
  </div>
</template>

<script>
export default {
  name: "SocialNavbar",
};
</script>

<style scoped>
.social-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 15px;
}

img {
  width: 40px;
  height: auto;
  margin-right: 10px;
  transition: transform 0.4s ease-in-out;
}

img:hover {
  transform: rotate(360deg);
}
</style>
