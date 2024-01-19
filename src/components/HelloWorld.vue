<template>
  <div>
    <p>coucou {{ personne.prenom }}</p>
    <p>Props recue : {{ message }}</p>
    <p>URL linked : {{ link }} </p>
  </div>
</template>

<script setup>
import { ref } from "vue";

defineProps({
  message : String,
  link : String,
})

const prenom = "saad";
const personne = ref({
  prenom : "Matthieu",
  age: 42
})

const url = "https://google.com";

const afficherPrenom = (prenom) => {
  console.log("Bonjour" + prenom);
}
</script>
