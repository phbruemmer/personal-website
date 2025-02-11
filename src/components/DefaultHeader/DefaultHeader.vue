<template>
  <div class="header-container">
    <!-- Back -->
    <RouterLinks reference="/">Back</RouterLinks>

    <!-- Logo -->
    <Logo />
  </div>
</template>
<script>
import Logo from "@/components/Defaults/Logo.vue";
import RouterLinks from "@/components/Defaults/RouterLinks.vue";

export default {
  name: "MainHeader",
  components: {
    Logo,
    RouterLinks,
  },
};
</script>

<style>
.header-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
