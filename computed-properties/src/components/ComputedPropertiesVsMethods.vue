<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  computed: {
    time() {
      const date = new Date();
      return `${date.getHours()}:${date.getMinutes()}:${date.getSeconds()}`
    }
  },
  methods: {
    getTime() {
      const date = new Date();
      return `${date.getHours()}:${date.getMinutes()}:${date.getSeconds()}`
    }
  }
}
</script>

<template>
  <p>{{ time }}</p>
  <p>{{ getTime() }}</p>
  <p>{{ count }} N° Atualizações do Template:</p>
  <button @click="count++">Incrementar +1</button>
  <p>
    Note que utilizando a função(getTime) o template é atualizado a cada alteração de outras propriedades(dependências) reativas,<br>
    isso tornara o template inchados e difíceis de manter em uma escala maior.
  </p>
</template>

<!--
  A diferença de utilizar as 'Computed Properties' ao inves de funções normais é que 
  as propriedades computadas são armazenadas em cache com base em suas 'dependências reativas'.

  Ou seja, uma propriedade computada só será atualizará quando algumas de suas 'dependências reativas' forem alteradas.

  O ideal em grande parte das vezes, é utilizar as 'Computed Properties' no template na exibição de informações e
  as functions/methods quando for realizada alguma operação logica de funcionalidade.
-->

<!--
  Por que precisamos de cache?

  Imagine que temos uma propriedade computada cara, uma lista de itens por exemplo,
  que requer fazer um loop através de uma enorme matriz e fazer muitos cálculos.
  Então podemos ter outras propriedades computadas que, por sua vez, dependem de list.

  Sem cache, estaríamos executando uma lista getter's muito mais vezes do que o necessário!
  Nos casos em que você não deseja armazenar em cache, use uma chamada de método.
-->