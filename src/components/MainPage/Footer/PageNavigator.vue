<template>
  <div class="link-container">
    <a :href="reference" @click.prevent="scrollToTarget"><slot /></a>
  </div>
</template>

<script>
export default {
  name: "Links",
  props: {
    reference: {
      type: String,
      required: true,
    },
  },

  methods: {
    scrollToTarget() {
      const element = document.getElementById(this.reference);

      if (element) {
        element.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      } else {
        console.error("Couldn't find: " + this.reference);
      }
    },
  },
};
</script>

<style scoped>
a {
  margin: 0 10px;
  text-decoration: none;
  color: #333;
  font-family: Arial, Helvetica, sans-serif;
}

a:hover {
  text-decoration: underline;
}
</style>
