<template>
  <div class="separator-container">
    <div class="line"></div>
    <h2 class="separator-text"><slot /></h2>
    <div class="line"></div>
  </div>
</template>

<script>
export default {
  name: "SectionSeparator",
};
</script>

<style scoped>
.separator-container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
  gap: 15px;
  position: relative;
  padding: 20px 0;
  animation: fadeIn 1s ease-in-out forwards;
}

.line {
  flex-grow: 1;
  height: 2px;
  background: #b6bfc3c7;
  border-radius: 50px;
}

.separator-text {
  font-size: 1.8rem;
  font-weight: 700;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding: 10px 20px;
  background: rgba(169, 169, 169, 0.836);
  backdrop-filter: blur(5px);
  border-radius: 12px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.separator-text:hover {
  cursor: default;
}
</style>
