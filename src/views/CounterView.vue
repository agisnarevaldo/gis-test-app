<script setup>
import { ref } from "vue";

const count = ref(0)
</script>
<template>
    <div class="counter">
        <button @click="count++">+</button>
        <h1>{{ count }}</h1>
        <button @click="count--">-</button>
    </div>
</template>
<style>
@media (min-width: 1024px) {
  .counter {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
  button {
    font-weight: bold;
    padding: 5px 10px;
  }
}
</style>
