<template>
  <div class="hello">
    <h2>{{ msg }}</h2>
    <p>
      A simple component demonstrating Vue's features.
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.hello {
  margin: 20px auto;
  padding: 20px;
  background-color: #f8f8f8;
  border-radius: 8px;
  max-width: 600px;
}
</style>