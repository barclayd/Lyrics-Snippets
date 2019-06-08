<template>
  <div class="text-center header">
    <h4>Quotes Added</h4>
    <div class="progress new-quote">
      <div
        class="progress-bar progress-bar-striped progress-bar-animated"
        role="progressbar"
        aria-valuenow="75"
        aria-valuemin="0"
        aria-valuemax="100"
        :style="{ width: percentage + '%' }"
      >
        {{ percentage > 0 ? `${percentage / 10}/${maxQuotes}` : null }}
      </div>
    </div>
  </div></template
>

<script>
export default {
  props: ['percentage', 'maxQuotes'],
  name: 'ProgressBar',
};
</script>

<style scoped>
.header {
  margin: 50px 20px;
}
</style>
