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

  <!-- Tag do componente Hyperlink -->
  <Hyperlink/>

  <p>
    Os aplicativos Vue são organizados em uma árvore de componentes aninhados e reutilizáveis.<br>
    Por exemplo, a árvore de componentes de um aplicativo To-Do pode ter esta aparência:
  </p>

  <textarea v-pre disabled style="width: 624px; height: 155px;">
    App (root component)
    ├─ TodoList
    │  └─ TodoItem
    │     ├─ TodoDeleteButton
    │     └─ TodoEditButton
    └─ TodoFooter
       ├─ TodoClearButton
       └─ TodoStatistics
  </textarea>

</template>

<style>
h1 {
  color: #42B883;
}
</style>
