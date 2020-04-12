<template>
  <header class="header">
    <h1 class="page-h1">{{ pageTitle }}</h1>
    <Button variant="secondary" title="Добавить" />
  </header>
</template>

<script>
import Button from './_common/Button.vue';

export default {
  props: ['pageTitle', 'withButton'],
  components: {
    Button
  }
};
</script>

<style>
.header {
  margin-top: 24px;
  margin-bottom: 48px;
  display: flex;
}

.page-h1 {
  margin: 0;
  margin-right: 24px;
}
</style>
