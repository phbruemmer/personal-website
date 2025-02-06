<template>
  <div class="header-container">
    <!-- Logo -->
    <Logo />
    <!-- Navbar -->
    <Navbar />
    <!-- Links / Socials -->
    <SocialNavbar />
  </div>
</template>
<script>
import Logo from "@/components/MainHeader/Logo.vue";
import Navbar from "@/components/MainHeader/Navbar.vue";
import SocialNavbar from "@/components/MainHeader/SocialNavbar.vue";

export default {
  name: "MainHeader",
  components: {
    Logo,
    Navbar,
    SocialNavbar,
  },
};
</script>

<style>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  pad: 10px;
}
</style>
