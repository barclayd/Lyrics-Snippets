<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote" :style="textColour(idx)">
        <slot />
      </div>
    </div></div
></template>

<script>
export default {
  props: ['idx'],
  methods: {
    textColour(idx) {
      if (idx % 2 === 0) {
        return {
          color: '#6670ba',
        };
      }
    },
  },
};
</script>

<style scoped>
.panel-body {
  font-family: 'Pacifico', cursive;
  font-size: 24px;
  color: #66a8ba;
  border: 1px solid #d3d3d3;
  border-radius: 10px;
  padding: 20px;
}

.quote {
  cursor: pointer;
  margin: 10px;
}

.quote:hover {
  background-color: #ff8e8d;
}
</style>
