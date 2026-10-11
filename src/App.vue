<script setup>
const massage = 'Hello Vue 3 + Vite'
const name = '5no0p'
const date = '2026'
</script>

<template>
  <div class="template">
    <main>
      <h1>{{ massage }}</h1>
    </main>
    <footer>
      <p>&copy; {{ date }} {{ name }}. All rights reserved.</p>
    </footer>
  </div>
</template>

<style scoped>
.template {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: #282c34;
}
h1 {
  font-weight: bold;
  text-align: center;
  color: white;
}
p {
  text-align: center;
  color: white;
}
footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  color: white;
  text-align: center;
  font-family: monospace;
}
</style>
