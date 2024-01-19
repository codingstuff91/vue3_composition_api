<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld :message="coucou" :link="url" />
  <form action="#">
    <input type="text" v-model="name">
    
    <input type="string" v-model.lazy="counter">

  </form>
</template>

<script setup>
import { ref, watch } from 'vue';
import HelloWorld from './components/HelloWorld.vue';

const url = ref('https://google.com');
const image_path = "./assets/logo.png";

const name = ref('Mike');

const counter = ref('John');

watch(counter, (newValue, oldValue) => {
  console.log('ancienne valeur', oldValue);
  console.log('nouvelle valeur', newValue);
})

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
