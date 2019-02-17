<template>
  <div class="row">
    <app-note @click.native="deleteNote(index)" v-for="(note,index) in notes" :key="index">{{note}}</app-note>
  </div>
</template>

<script>
import Note from "./Note.vue";
export default {
  props: {
    notes: {
      type: Array
    }
  },
  components: {
    appNote: Note
  },
  methods: {
    deleteNote(index) {
      this.notes.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
