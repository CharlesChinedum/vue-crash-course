<script setup lang="ts">
import { onMounted } from 'vue';


import Header from '../components/Header.vue';
import Tasks from '../components/Tasks.vue'

let tasks: {
  id: number,
  text: string,
  day: string,
  reminder: boolean,
}[] = []

// onMounted(() => {
  tasks = [
    {
      id: 1,
      text: 'Doctors Appointment',
      day: 'Feb 5th at 2:30pm',
      reminder: true,
    }, {
      id: 2,
      text: 'Meeting at School',
      day: 'Feb 6th at 1:30pm',
      reminder: true,
    }, {
      id: 3,
      text: 'Food Shopping',
      day: 'Feb 5th at 2:30pm',
      reminder: false,
    }
  ]

  // console.log(tasks)
// })
</script>

<template>
  <main>
    <Header title="Task Tracker" />
    <Tasks :tasks="tasks" />
  </main>
</template>
