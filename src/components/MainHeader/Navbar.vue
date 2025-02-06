<template>
  <div class="navbar-container">
    <Link reference="Kombi">Home</Link>
    <Link reference="Kombi">About</Link>
    <Link reference="Kombi">Projects</Link>
    <Link reference="Kombi">Prototypes</Link>
  </div>
</template>

<script>
import Link from "@/components/MainHeader/Links.vue";

export default {
  name: "Navbar",
  components: {
    Link,
  },
};
</script>

<style scoped>
.navbar-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 120px;
}
</style>
