<template>
  <nav>
    <router-link :to="{ name: 'home' }">Home</router-link>
    <router-link :to="{ name: 'about' }">About</router-link>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  align-items: center;
}
nav > * {
  margin-right: 1rem;
  color: green;
}
</style>
