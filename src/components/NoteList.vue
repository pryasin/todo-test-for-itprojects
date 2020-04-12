<template>
  <main class="notes">
    <Note v-for="note in notes" :notes="notes" :key="note.id" :note="note" />
  </main>
</template>

<script>
import Note from './Note.vue';

export default {
  props: ['notes'],
  components: { Note }
};
</script>

<style>
.notes {
  display: flex;
  flex-wrap: wrap;
}
</style>
