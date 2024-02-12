<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <h1> Dokkaebi Bag </h1>
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <nav class="linksRouters">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/cart">Cart</RouterLink>
      </nav>
    </div>
  </header>
  
</template>

<style scoped>
*{
  padding: 1%;
  text-align: center;
}

h1{
  text-align: center;
  font-weight: bold;
}

.linksRouters{
  color:black;
}
</style>
