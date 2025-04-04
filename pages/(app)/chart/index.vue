<template>
  <div>
    <div class="h1">Chart page</div>

    <div id="chart">
      <svg ref="svg"></svg>
    </div>
  </div>
</template>

<script>
import * as d3 from "d3";

export default {
  name: "Chart",
  mounted() {
    this.createChart();
  },
  methods: {
    createChart() {
      const data = [30, 86, 168, 281, 303, 365];
      const width = 500;
      const height = 300;

      const svg = d3
        .select(this.$refs.svg)
        .attr("width", width)
        .attr("height", height);

      svg
        .selectAll("rect")
        .data(data)
        .enter()
        .append("rect")
        .attr("x", (d, i) => i * 70)
        .attr("y", (d) => height - d)
        .attr("width", 65)
        .attr("height", (d) => d)
        .attr("fill", "#69b3a2");
    },
  },
};
</script>

<style>
svg {
  border: 1px solid black;
}
</style>
