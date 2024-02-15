<!-- name files two words, otherwise there may be issues -->
<template>
    <div>
        <h2> {{ Item.name }} </h2>
        <img :src="Item.image" alt="">
        <h3> {{ clicked }}</h3>
        <button @click="increment"> Click Me </button>
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
    img{
        width: 250px;
        height: 300px;
        object-fit: cover;
    }
</style>