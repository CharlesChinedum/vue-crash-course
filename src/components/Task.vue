<script setup lang="ts">

    defineProps<{
        task: Object,
    }>()
</script>

<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>{{task.text}}
            <!-- TODO: resolve fontawesome error -->
        <i class="fas fa-times"></i>
        </h3>
        <p>{{task.day}}</p>
    </div>
</template>

<style scope>
.fas {
    color: red;
}
    .task {
        border-bottom: 1px solid #ccc;
        cursor: pointer;
        padding: 10px 20px;
        margin: 10px 0;
    }
    .task.reminder {
        border-left: 5px solid green;
    }
    .task h3 {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>