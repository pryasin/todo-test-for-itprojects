<template>
  <div class="container">
    <Header pageTitle="Заметки" />
    <NoteList :notes="notes" />
  </div>
</template>

<script>
import Button from './components/_common/Button.vue';
import Header from './components/Header.vue';
import NoteList from './components/NoteList.vue';

export default {
  data: function() {
    return {
      notes: [
        {
          id: 1,
          title: 'Сайт',
          todos: ['Добавить слайдер', 'Обновить favicon']
        },
        {
          id: 2,
          title: 'Продукты',
          todos: ['Купить бананы', 'Купить молоко', 'Купить макароны']
        },
        {
          id: 3,
          title: 'Сломанный чайник',
          todos: ['Одолжить инструменты у Леши', 'Посмотреть уроки на ютюбе']
        },
        {
          id: 4,
          title: 'Отпуск',
          todos: ['Посмотреть путевки', 'Купить билеты', 'Взять страховку']
        },
        {
          id: 5,
          title: 'Vue',
          todos: ['Почитать доки', 'Настроить рабочее окружение']
        }
      ]
    };
  },
  components: {
    Button,
    Header,
    NoteList
  }
};
</script>

<style scoped>
.container {
  padding-left: 32px;
  padding-right: 16px;
}
</style>
