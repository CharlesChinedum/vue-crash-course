<script setup lang="ts">
defineProps<{
  name: string,
  color: string,
}>()

const handleClick = () => {
    console.log('clicked')
}

</script>

<template>
    <button @click="handleClick" :style="{backgroundColor: color}">{{ name }}</button>
</template>

<style>
button {
    padding: 5px 20px;
    border: none;
    border-radius: 5px;
    color: white;
    cursor: pointer;
    font-size: 1.2rem;
    font-weight: 500;
    transition: all 0.3s ease;
}
</style>