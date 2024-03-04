<template>
  <div class="card">
    <h2>{{ Destination.name }}</h2>
    <h3>{{ Destination.desc }}</h3>
    <img :src="Destination.image" :alt="Destination.imageDesc" />
    <h3>{{ clicked }}</h3>
    <button @click="increment">Add to Cart</button>
  </div>
</template>
  
<script setup>
import { ref } from "vue";
const props = defineProps({
  Destination: Object,
});

  //clicker logic
let clicked = ref(0);
function increment() {
  clicked.value++;
}

</script>

<style scoped>
</style>