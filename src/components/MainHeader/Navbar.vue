<template>
  <div class="navbar-container">
    <Link reference="#">Home</Link>
    <Link reference="#">About</Link>
    <Link reference="#">Projects</Link>
    <Link reference="#">Prototypes</Link>
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
