<template>
  <footer>
    <div class="content">
      <img src="@/assets/signature.png" alt="logo" />
      <nav>
        <PageNavigator reference="Home">Home</PageNavigator>
        <PageNavigator reference="About">About</PageNavigator>
        <PageNavigator reference="Projects">Projects</PageNavigator>
      </nav>
      <p><i>© 2025 ~ phbruemmer</i></p>
      <div class="social-links">
        <a href="https://github.com/phbruemmer" target="_blank">GitHub</a>
        <a href="https://www.instagram.com/phbruemmer/" target="_blank"
          >Instagram</a
        >
        <a href="https://x.com/1Phbruemmer" target="_blank">Twitter</a>
        <a href="https://discord.gg/a2h5feJ8aV" target="_blank">Discord</a>
      </div>
      <button @click="scrollToTop">~ Back to Top ~</button>
    </div>
  </footer>
</template>

<script>
import PageNavigator from "@/components/MainPage/Footer/PageNavigator.vue";

export default {
  name: "Footer",
  components: {
    PageNavigator,
  },
  methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
  },
};
</script>

<style scoped>
footer {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
  margin-top: 10vh;
  background-color: #fffbf3;
  height: 30vh;
  border-radius: 60px;
  box-shadow: 0px -4px 10px rgba(0, 0, 0, 0.1);
  padding: 20px;
}
a {
  margin: 0 10px;
  text-decoration: none;
  color: #333;
  font-family: Arial, Helvetica, sans-serif;
}

a:hover {
  text-decoration: underline;
}

p {
  font-family: Arial, Helvetica, sans-serif;
  color: #333;
  transition: transform 0.3s ease-in-out;
}

p:hover {
  cursor: default;
  transform: scale(0.9);
}

nav {
  display: flex;
  justify-content: space-around;
}

button {
  margin-top: 2vh;
  padding: 5px 10px;
  border: none;
  background-color: #b7b5b3;
  color: white;
  cursor: pointer;
  border-radius: 5px;
  transition: transform 0.3s ease-in-out;
}
button:hover {
  transform: scale(1.025);
}

img {
  width: 200px;
  height: auto;
  margin: 20px;
  transition: transform 0.3s ease-in-out;
}

img:hover {
  transform: scale(1.04);
}
</style>
