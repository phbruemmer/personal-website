<template>
  <div class="diagram-container">
    <svg viewBox="0 0 100 100" class="progress-circle">
      <circle class="bg" cx="50" cy="50" r="45"></circle>

      <circle
        class="progress"
        cx="50"
        cy="50"
        r="45"
        :stroke-dasharray="circumference"
        :stroke-dashoffset="progressOffset"
        transform="rotate(-90 50 50)"
      ></circle>

      <text x="50" y="55" text-anchor="middle" class="percentage">
        {{ progress }}%
      </text>
    </svg>
    <p><slot /></p>
  </div>
</template>

<script>
export default {
  name: "Diagram",
  props: {
    progress: {
      type: Number,
      required: true,
    },
  },
  computed: {
    circumference() {
      return 2 * Math.PI * 45;
    },
    progressOffset() {
      return this.circumference * (1 - this.progress / 100);
    },
  },
};
</script>

<style scoped>
.diagram-container {
  width: 120px;
  height: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.progress-circle {
  width: 100%;
  height: 100%;
}

circle {
  fill: none;
  stroke-width: 8;
  stroke-linecap: round;
  transition: stroke-width 0.2s ease-in-out;
}

circle:hover {
  stroke-width: 10;
}

.bg {
  stroke: #e0e0e0;
}

.progress {
  stroke: #4caf50;
  transition: stroke-dashoffset 0.5s ease;
}

.percentage {
  font-size: 14px;
  font-family: Arial, Helvetica, sans-serif;
  fill: black;
  font-weight: bold;
}

p {
  font-family: Arial, Helvetica, sans-serif;
  font-weight: 100;
}
</style>
