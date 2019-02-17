<template>
  <div class="col-sm-4 col-md-4 col-lg-3 col-xs-6">
    <div class="note">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
div.note {
  border: 2px solid #ccc;
  border-radius: 5px;
  min-height: 80px;
  vertical-align: center;
  cursor: pointer;
  margin: 10px auto;
}
div.note:hover {
  background-color: rgb(245, 207, 207);
}
</style>
