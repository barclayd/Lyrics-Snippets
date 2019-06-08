<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <slot />
      </div>
    </div>
  </div></template>

<script>
</script>

<style scoped>
  .panel-body {
    font-family: 'Pacifico', cursive;
    font-size: 24px;
    color: #778899;
    border: 1px solid #D3D3D3;
    border-radius: 10px;
    padding: 20px;
  }

  .quote.panel-body:nth-child(even) {
    color: blueviolet !important;
  }

  .quote {
    cursor: pointer;
    margin: 10px;
  }

  .quote:hover {
    background-color: #ff8e8d;
  }
</style>
