<template>
  <svg width="200" height="600" viewBox="0 0 200 600">
    <path
      d="M100 10 C 120 100, 50 150, 100 200 
       S 150 300, 100 350 
       S 50 450, 100 500"
      stroke="#616161"
      fill="none"
      stroke-width="2"
      stroke-dasharray="6"
    />

    <g v-for="(point, index) in points" :key="index">
      <a :xlink:href="point.href" target="_blank">
        <circle :cx="point.x" :cy="point.y" r="5" fill="black" />
        <text :x="point.x + 14" :y="point.y + 3.5" font-size="9" fill="#616161">
          {{ point.label }}
        </text>
      </a>
    </g>
  </svg>
</template>

<script>
export default {
  name: "Path",
  data() {
    return {
      points: [
        { x: 100, y: 10, label: "2006 ~ January", href: "www.wikipedia.de" },
        { x: 100, y: 200, label: "2022 ~ First degree", href: "" },
        { x: 100, y: 350, label: "2025 ~ Second degree", href: "" },
        { x: 100, y: 500, label: "~ Future ~", href: "" },
      ],
    };
  },
};
</script>

<style scoped>
circle {
  stroke: white;
  stroke-width: 2;
  transition: stroke-width 0.2s ease-in-out;
}

circle:hover {
  stroke-width: 0;
  cursor: pointer;
}

svg {
  height: 100vh;
  width: auto;
}
</style>
