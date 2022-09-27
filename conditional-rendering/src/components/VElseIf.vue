<script>
export default {
  data() {
    return {
      type: '0'
    }
  }
}
</script>

<template>
  <h2>Conditional v-else-if</h2>

  <p>
    O <i>v-else-if</i>, como o nome sugere, serve como um bloco "else if" para <i>v-if</i>.<br>
    Também pode ser encadeado várias vezes:
  </p>

  <p v-if="type === '1'">🍉🍊🍍 Fruits</p>
  <p v-else-if="type === '2'">🥒🥦🥕 Vegetable</p>
  <p v-else-if="type === '3'">🥀🌷🌻 Flowers</p>
  <p v-else>Not 🍉/🥦/🌻</p>


  <!--
    Ignore this code snippet, you can learn about clicking on the (Form Input Bindings) subproject!
    https://vuejs.org/guide/essentials/forms.html#v-model-with-components
  -->
  <select v-model="type">
    <option value="1">Fruits</option>
    <option value="2">Vegetable</option>
    <option value="3">Flowers</option>
  </select>

</template>