<template>
  <div>
    <form @submit.prevent="addNote">
      <div class="row">
        <div class="form-group">
          <div class="col-sm-12">
            <textarea rows="5" cols="100" v-model="noteValue"></textarea>
          </div>
        </div>
        <div class="form-group">
          <div class="col-sm-12">
            <button class="btn btn-primary">Add Note</button>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      noteValue: ""
    };
  },
  methods: {
    addNote() {
      if (this.noteValue.trim() != "") {
        this.$emit("addedNote", this.noteValue);
        this.noteValue = "";
      } else {
        alert("Note cannot be empty!");
      }
    }
  }
};
</script>

<style>
</style>
