<template>
  <div id="app">
    <div class="container">
      <app-progress :noteCount="notes.length" :maxNoteCount="maxNoteCount"></app-progress>
      <app-new-note @addedNote="addNote"></app-new-note>
      <app-note-grid :notes="notes"></app-note-grid>
    </div>
  </div>
</template>

<script>
import NoteGrid from "./components/NoteGrid.vue";
import NewNote from "./components/NewNote.vue";
import Progress from "./components/Progress.vue";

export default {
  name: "app",
  data() {
    return { maxNoteCount: 10, notes: ["Note 1", "Note 2"] };
  },
  methods: {
    addNote(value) {
      if (this.notes.length < 10) {
        this.notes.push(value);
      } else {
        alert("Please delete note before add note");
      }
    }
  },
  components: {
    appNoteGrid: NoteGrid,
    appNewNote: NewNote,
    appProgress: Progress
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
