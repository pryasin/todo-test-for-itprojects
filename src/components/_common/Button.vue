<template>
  <button :class="['btn', variant]" type="submit">{{ title }}</button>
</template>

<script>
export default {
  props: ['title', 'variant']
};
</script>

<style scoped>
.btn {
  box-sizing: border-box;
  border-radius: 6px;
  padding: 10px 30px;
  font-weight: 600;
  font-size: 14px;
  appearance: none;
  transition: all 0.3s;
}

.primary {
  background-color: #355eed;
  border: 2px solid #355eed;
  color: #fff;
}

.primary:hover {
  background-color: #577bf6;
  border: 2px solid #577bf6;
}

.secondary {
  color: #355eed;
  background-color: #fff;
  border: 2px solid #355eed;
}

.secondary:hover {
  color: #577bf6;
  background-color: #fff;
  border: 2px solid #577bf6;
}

.secondary:hover,
.primary:hover,
.secondary:active,
.primary:active {
  transition: none;
}

.secondary:active,
.primary:active {
  border: 2px solid #2b4ec9;
  background-color: #2b4ec9;
}

.secondary:active {
  color: #fff;
}
</style>
