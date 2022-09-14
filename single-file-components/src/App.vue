<script>
import Hyperlink from './components/Hyperlink.vue';

export default {
  components: {
    Hyperlink
  }
}
</script>

<template>
  <h1>Single-File Components</h1>
  <p>
    Vue Single-File Components (também conhecido como arquivos *.vue, abreviado como SFC)<br>
    é um formato de arquivo especial que nos permite encapsular o modelo, a lógica e o estilo<br>
    de um componente Vue em um único arquivo.
  </p>

  <Hyperlink></Hyperlink>

</template>

<style>
h1 {
  color: #42B883;
}
</style>
