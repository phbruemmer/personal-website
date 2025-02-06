<template>
  <div class="navbar-container">
    <Link reference="Home">Home</Link>
    <Link reference="About">About</Link>
    <Link reference="Projects">Projects</Link>
    <Link reference="Prototypes">Prototypes</Link>
  </div>
</template>

<script>
import Link from "@/components/MainHeader/Links.vue";
export default {
  name: "Navbar",
  components: { Link },
};
</script>

<style scoped>
.navbar-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  width: 100%;
  flex-wrap: wrap;
}
</style>
