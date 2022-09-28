<script>
export default {

  data() { // Use o método data para declarar o estado reativo de um componente!
    return {
      count: 1
    }
  },

  /*
    O 'mounted' é um gancho de ciclo de vida, mais detalhes no subprojeto (Lifecycle Hooks).
    https://vuejs.org/guide/essentials/lifecycle.html
  */
  mounted() {
    // 'this' refere-se à instância do componente.
    console.info(this.count)

    // Os dados também podem ser modificados!
    this.count = 2
  }

}
</script>

<template>
  <h2>Declarando Estado Reativo</h2>

  <p>
    Com a API Options, usamos a opção <i>data</i> para de declarar o estado reativo de um componente.<br>
    O valor da opção deve ser uma função que retorna um objeto.<br>
    Vue irá chamar a função ao criar uma nova instância de componente,<br>
    e encapsular o objeto retornado em seu sistema de reatividade.
  </p>

  <p>
    Quaisquer propriedades de nível superior deste objeto são proxies na instância do componente<br>
    (Use <i>this</i> em métodos e em ganchos de ciclo de vida):
  </p>


  <p>
    Essas propriedades de instância são adicionadas apenas quando a instância é criada pela primeira vez, portanto,<br>
    você precisa garantir que todas estejam presentes no objeto retornado pela datafunção.<br>
    Quando necessário, use <i>null</i> e <i>undefined</i> ou algum outro valor de espaço reservado para propriedades<br>
    em que o valor desejado ainda não esteja disponível.
  </p>

  <p>
    É possível adicionar uma nova propriedade diretamente thissem incluí-la no data.<br>
    No entanto, as propriedades adicionadas dessa maneira não poderão acionar atualizações reativas.
  </p>

</template>