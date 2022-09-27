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
  <h2>Conditional v-if</h2>

  <p>
    A diretiva <i>v-if</i> usada para renderizar condicionalmente um bloco.<br>
    O bloco só será renderizado se a expressão da diretiva retornar um valor verdadeiro.
  </p>

  <p v-if="awesome">Vue é incrível!</p>

</template>