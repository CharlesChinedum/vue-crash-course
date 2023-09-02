<script setup lang="ts">
import Button from './Button.vue'

defineProps<{
  title: string
}>()


</script>

<template>
  <header>
    <h1>{{ title }}</h1>
    <Button name="Add Task" color="green" />
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center ;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
