<script>
export default {
  data() {
    return {
      author: {
        name: 'John Doe',
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      }
    }
  },
  computed: {
    publishedBooks() {
      return this.author.books.length > 0 ? 'Sim' : 'Não'
    }
  }
}
</script>

<template>
  <p>Autor: {{ author.name }}</p>
  <p>O autor já possui livros publicados? {{ publishedBooks }}</p>

  <p>Livros</p>
  <ul>
    <li v-for="book in author.books">{{ book }}</li>
  </ul>
</template>

<!--
  As expressões no template são muito convenientes, mas destinam-se a operações simples.
  Colocar muita lógica em seus templates pode torná-los inchados e difíceis de manter.

  Portanto utilizaremos as Propriedades Computadas para resolver esse problema.
-->

<!--
  Uma propriedade computada rastreia automaticamente suas dependências reativas.
  O Vue está ciente de que o cálculo de 'publishedBooks' de author.books, portanto, ele atualizará
  quaisquer ligações que dependam de 'publishedBooks' quando author.books for alterado.
-->