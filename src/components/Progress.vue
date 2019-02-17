<template>
  <div class="container-progress">
    <div class="progress">
      <div
        class="progress-bar"
        role="progressbar"
        aria-valuenow="0"
        aria-valuemin="0"
        aria-valuemax="100"
        :style="{width:(noteCount/maxNoteCount*100)+'%'}"
      >{{noteCount}} / {{maxNoteCount}}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    noteCount: {
      type: Number,
      required: true
    },
    maxNoteCount: {
      type: Number,
      required: true
    }
  }
};
</script>

<style scoped>
.container-progress {
  margin: 30px auto;
}
</style>
