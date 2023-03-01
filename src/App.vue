<template>
  <section class="container">
    <h2>{{ user.userName }}</h2>
    <h3>{{ user.age }}</h3>
  </section>
</template>

<script setup>
import { reactive } from "vue";
// const userName = ref("Maximilian"); // ref for all kind of data: number, string, onject. user.value.userName = "Kirill";
// const age = ref(32);
const user = reactive({
  userName: "Maximilian",
  age: 32,
}); // reactive for onject only and. user.userName = "Kirill";
setTimeout(function () {
  user.userName = "Kirill";
  user.age = 20;
}, 2000);

// return { userName: name };
// data() {
//   return {
//     userName: 'Maximilian',
//   };
// },
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>
