<script>
export default {
  data() {
    return {
      awesome: true
    }
  }
}
</script>

<template>
  <h2>Conditional v-else</h2>

  <p>
    Você pode usar a <i>v-else</i> diretiva para indicar um "bloco else" para <i>v-if</i>:
  </p>

  <p v-if="awesome">Vue é incrível!</p>
  <p v-else>Oh no 😢</p>
  
  <!-- 
    Ignore this code snippet, you can learn about clicking on the (Event Handling) subproject!
    https://vuejs.org/guide/essentials/event-handling.html
  -->
  <button @click="awesome = !awesome">Alternar</button>

</template>