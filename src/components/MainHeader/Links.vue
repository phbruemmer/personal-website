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
      const element = document.querySelector(this.reference);

      if (element) {
        element.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      }
    },
  },
};
</script>

<style scoped>
a {
  font-size: 16px;
  font-weight: 100;
  font-family: Arial, Helvetica, sans-serif;
  display: inline-block;
  position: relative;
  text-decoration: none;
  color: #000;
}

a::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #000;
  transition: width 0.2s ease;
}

a:hover::after {
  width: 100%;
}

a:hover {
  cursor: pointer;
}
</style>
