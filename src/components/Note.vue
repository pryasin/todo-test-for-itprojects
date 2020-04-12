<template>
  <article class="card">
    <h2 class="note-title">{{ note.title }}</h2>
    <div class="note-line"></div>
    <ul class="todo-list">
      <li
        @click="goToDetails(note.id)"
        :key="index"
        v-for="(todo, index) in note.todos"
        class="todo-list-item"
      >
        {{ todo }}
      </li>
    </ul>
    <trash-2-icon size="1.5x" class="delete-icon"></trash-2-icon>
  </article>
</template>

<script>
import { Trash2Icon } from 'vue-feather-icons';

export default {
  components: {
    Trash2Icon
  },
  props: ['note']
};
</script>

<style>
.card {
  flex-grow: 1;
  padding-top: 16px;
  padding-bottom: 24px;
  margin-right: 16px;
  margin-bottom: 16px;
  background-color: #f0f0f0;
  border-radius: 8px;
  position: relative;
  cursor: default;
  min-width: 400px;
}

.card:hover {
  background-color: #e1e8ff;
}

.note-title {
  margin: 0;
  padding-bottom: 16px;
  margin-left: 16px;
}

.todo-list {
  margin-top: 16px;
  padding-left: 16px;
  font-size: 14px;
  margin-left: 16px;
}

.todo-list-item {
  margin-bottom: 8px;
  color: #4e4e4e;
}

.delete-icon {
  position: absolute;
  bottom: 0;
  right: 0;
  color: #9f9f9f;
  padding: 8px;
}

.delete-icon:hover {
  color: #ef5350;
}

.note-line {
  width: 100%;
  border-bottom: 2px solid rgba(0, 0, 0, 0.04);
}
</style>
