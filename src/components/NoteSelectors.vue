<template>
  <div class="note-selectors">
    <NoteSelector 
      v-for="note in notes" 
      v-bind:note="note" 
      v-bind:key="note.id"
    />
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector.vue";
export default {
  data: function () {
    return {
      notes: [
        { id: 1, body: "Note 1", timestamp: Date.now() },
        { id: 2, body: "Note 2", timestamp: Date.now() },
        { id: 3, body: "Note 3", timestamp: Date.now() },
        { id: 4, body: "Note 4", timestamp: Date.now() },
      ],
      selectedNoteId: 1,
    };
  },
  components: {
    NoteSelector,
  },
};
</script>
