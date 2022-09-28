<script>
import { debounce } from 'lodash-es'

export default {
  methods: {

    beforeMethod() {
      console.info('Before Debounced Method');
    },

    method: debounce(function () {
      console.info('Lodash Debounced Method');
    }, 500)

  }
}
</script>

<template>
  <h2>Métodos com estado</h2>

  <p>
    Em alguns casos, podemos precisar criar dinamicamente uma função de método, por exemplo,<br>
    criando um manipulador de eventos <i>debounced</i> do <i>Lodash</i>.
  </p>

  <p>
    O manipulador de eventos <i>debounced</i> do <i>Lodash</i> cria uma função que atrasa a invocação<br>
    até que os milissegundos de espera tenham decorrido desde a última vez que a função debounced foi invocada.<br>
    A função debounced vem com um método cancel para cancelar invocações de funções atrasadas e um método flush para invocá-las imediatamente.<br>
    Forneça opções para indicar se a função deve ser invocado na borda inicial e/ou final do tempo limite de espera. <br>
    O <i>função</i> é invocado com os últimos argumentos fornecidos à função debounced.<br>
    Chamadas subsequentes para a função debounced retornam o resultado da última invocação de função.
  </p>

  <button @click="beforeMethod(); method();">Chamar função com Debounced: {{ count }}</button>

  <p>
    No entanto, essa abordagem é problemática para componentes que são reutilizados porque uma função debounced é <i>stateful</i><br>
    Ou seja, ela mantém algum estado interno no tempo decorrido.<br>
    Se várias instâncias de componentes compartilharem a mesma função depurada, elas interferirão umas nas outras.
  </p>

  <p>
    Para manter a função debounced de cada instância do componente independente das outras,<br>
    podemos criar a versão debounced no createdgancho do ciclo de vida:
  </p>

  <textarea v-pre disabled style="width: 624px; height: 260px;">
    export default {
      created() {
        // Cada instância agora tem sua própria cópia do manipulador Debounced
        this.debouncedClick = _.debounce(this.click, 500)
      },
      unmounted() {
        // Também é uma boa ideia cancelar o timer, quando o componente é removido
        this.debouncedClick.cancel()
      },
      methods: {
        click() {
          // Ação do método click()
        }
      }
    }
  </textarea>

</template>