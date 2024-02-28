<template>
    <div>
        <h2> {{ Item.name }} </h2>
        <img :src="Item.image" alt="">
        <h3> {{ clicked }}</h3>
        <button class="clickMeB" @click="increment"> Click Me </button>
    </div>
</template>

<script setup>
import { ref } from "vue";
const props = defineProps({
    Item: Object,
})

//clicker logic
const clicked = ref(0);
function increment(){
    clicked.value++;
}
</script>

<style scoped> 
*,
body,
html{
    background-color: white;
    color: #54585c;
}
img{
    width: 250px;
    height: 300px;
    object-fit: cover;
}
</style>