<template>
  <a :href="reference" @click.prevent="scrollToTarget"><slot /></a>
</template>

<script>
export default {
  name: "DefaultLink",
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
  font-size: 16px;
  color: #555;
  line-height: 1.5;
  text-decoration: None;
}

a:hover {
  text-decoration: underline;
}
</style>
