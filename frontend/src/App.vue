<script setup>
import axios from 'axios';

const login = async () => {
  await axios.get('sanctum/csrf-cookie');

  await axios.post('/login');
}
</script>

<template>
<form v-on:submit.prevent="login">
  <button type="submit">Login</button>
</form>
</template>

<style scoped>

</style>
