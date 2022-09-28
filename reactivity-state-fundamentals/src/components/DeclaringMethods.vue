<script>
export default {
  data() {
    return {
      count: 0
    }
  },

  methods: { // <= Declarção dos métodos é feita em 'methods'
    increment() {
      this.count++
    }
  },

  /*
    O 'mounted' é um gancho de ciclo de vida, mais detalhes no subprojeto (Lifecycle Hooks).
    https://vuejs.org/guide/essentials/lifecycle.html
  */
  mounted() { // Métodos podem ser chamados em ganchos de ciclo de vida ou outros métodos!
    this.increment()
  }
}
</script>

<template>
  <h2>Declarando Métodos</h2>

  <p>
    Para adicionar métodos a uma instância de componente, usamos a opção <i>methods</i>.<br>
    Este deve ser um objeto contendo os métodos desejados.
  </p>

  <button @click="increment">
    Chamando Metodos no Template: {{ count }}
  </button>

  <p>No exemplo acima, o método <i>increment</i> será chamado quando &lt;button&gt; for clicado.</p>

</template>