<script setup lang="ts">
import Task from './Task.vue'

defineProps<{
  tasks: any,
}>()

</script>

<template>
<div :key="task.id" v-for="task in tasks">
    <Task :task="task" />
</div>
</template>