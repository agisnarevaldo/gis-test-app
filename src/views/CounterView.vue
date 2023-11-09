<script setup>
import { ref } from "vue";

const count = ref(0)
</script>
<template>
    <div class="counter">
        <button @click="count++">
            {{ count }}
        </button>
    </div>
</template>
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>