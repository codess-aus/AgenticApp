<template>
  <div class="app">
    <header>
      <h1>User Management App</h1>
    </header>
    <main>
      <CreateUser />
    </main>
  </div>
</template>

<script>
import CreateUser from './components/CreateUser.vue'

export default {
  name: 'App',
  components: {
    CreateUser
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #f5f7fa;
  color: #2c3e50;
}

.app {
  text-align: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

header {
  margin-bottom: 40px;
}

h1 {
  font-weight: 500;
  font-size: 2.5em;
  margin-top: 0;
}

main {
  display: flex;
  justify-content: center;
}
</style>